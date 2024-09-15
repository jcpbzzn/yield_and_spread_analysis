# Yield and Spread Analysis

## Introduction

This repository contains classes of functions to calculate basic bond metrics such as price, yield to maturity, accrued interest, DV01, Modified Duration, Macaulay Duration, ecc... 
The purpose is not only to provide a useful bond math calculator, but also to provide a set of tools to experiment and visualise the impact of changes in the bond characteristics to their risk.

## Bond Math

The bond price P can be calculated using the following formula:

$$
P(r) = \sum_{t=1}^{T} \frac{C}{(1 + r)^t} + \frac{F}{(1 + r)^T}
$$

Where:
- P = Price of the bond
- C = Coupon payment
- r = Discount rate or yield to maturity
- t = Period
- T = Total number of periods until maturity
- F = Face value of the bond



