# Yield and Spread Analysis

## Introduction

This repository contains classes of functions to calculate basic bond metrics such as price, yield to maturity, accrued interest, DV01, Modified Duration, Macaulay Duration, ecc... 
The purpose is not only to provide a useful bond math calculator, but also to provide a set of tools to experiment and visualise the impact of changes in the bond characteristics to their risk.

## Bond Math

The bond clean price P on a coupon payment date can be calculated using the following formula:

$$
P = \sum_{t=1}^{T \cdot f} \frac{C/f}{(1 + r/f)^{t \cdot f}} + \frac{F}{(1 + r/f)^{T \cdot f}}
$$

Where:
- P = Price of the bond
- C = Coupon payment
- f = Coupon frequency
- r = Discount rate or yield to maturity
- t = Period
- T = Total number of periods until maturity
- F = Face value of the bond

To allow pricing in between coupon payment dates, we use the following formula [Boyles, Secrest, and Burney (2005)](#boyles2005):

$$
P = \sum_{t=1}^{T \cdot f} \frac{C/f}{(1+r/f)^{v \cdot f} \cdot (1 + r/f)^{(t-1) \cdot f}} + \frac{F}{(1+r/f)^{v \cdot f} \cdot (1 + r/f)^{(n-1) \cdot f}}
$$

Where:
- P = Price of the bond
- C = Coupon payment
- f = Coupon frequency
- r = Discount rate or yield to maturity
- t = Period
- T = Total number of periods until maturity
- n = total number of remaining years
- v = days between the settlement of the trade and the next coupon divided by the number of days in the coupon period.
- F = Face value of the bond

The accrued interest is calculated as follows [Saunders, Cornett, and Erhemjamts (2012)](#saunders2012):

$$
\text{Accrued Interest} = \frac{\text{Annual Coupon Payment}}{f} \cdot \frac{\text{Days Since Last Coupon}}{\text{Days in Coupon Period}}
$$

## References

- <a id="boyles2005"></a>Boyles, G. V., Secrest, T. W., & Burney, R. B. (2005). The Pricing of Bonds between Coupon Payments: From Theory to Market Practice. *Journal of Economics and Finance Education*, 4(2), 61.
- <a id="saunders2012"></a>Saunders, A., Cornett, M. M., & Erhemjamts, O. (2012). *Financial markets and institutions*. McGraw-Hill/Irwin.
