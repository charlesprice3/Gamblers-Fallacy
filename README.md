# Gambler’s Fallacy Simulation

## Background

The **Gambler’s Fallacy** is the belief that past results influence future ones in independent processes.

A common example appears in casinos. Many roulette tables display a **memory board** showing recent outcomes

```
┌─────┬─────┬─────┬─────┬────┬─────┬─────┬─────┬─────┬────┬─────┬─────┐
│ R34 │ R27 │ B26 │ R34 │ B2 │ B20 │ R34 │ B20 │ B33 │ R6 │ R18 │ R23 │
└─────┴─────┴─────┴─────┴────┴─────┴─────┴─────┴─────┴────┴─────┴─────┘
```

When a long streak appears, for example, Red occurring repeatedly, it often feels as though Black is now “due”.

This intuition comes from a perceived need for outcomes to balance.

---

## Why This Feels Illogical

Consider a fair coin.

- Probability of 1 head = 1/2  
- Probability of 2 heads in a row = (1/2)² = 1/4  
- Probability of 10 heads in a row = (1/2)¹⁰ = 1/1024  
- Probability of 11 heads in a row = (1/2)¹¹ = 1/2048  

So observing 10 or 11 heads consecutively is extremely unlikely.

Once such a streak occurs, it may seem irrational for the next flip to still have a 50% chance of being heads again. Intuitively, tails appears more likely because the sequence "should" begin to balance out to 50/50. 

---

## Independence of Trials

Coin flips are independent events. This means the next flip has no memory of prior outcomes.

P(next flip = T | previous k flips = H) = 0.5

This reads as:

The probability that the next flip is tails is still 50%, even if the previous k flips were all heads.

---

## Purpose of This Simulation

This project simulates millions of fair coin flips.

Each time a streak of k consecutive heads occurs, we:

- Record that a betting opportunity has appeared  
- Check whether the next flip is tails  
- Estimate:

P(next flip = T | previous k flips = H)

If the gambler’s fallacy were valid, this probability would exceed 0.5 after sufficiently long streaks.

This simulation tests whether that occurs.
