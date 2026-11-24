# Peanut butter sandwich

A **five-minute** lunch for one person.

## What you need

- 2 slices of bread
- Peanut butter
- Jam
  - Strawberry, if you have it

## Steps

1. Spread peanut butter on one slice.
2. Spread jam on the other.
3. Put them together and cut.

## For more people

| People | Slices of bread | Spoons of peanut butter |
|---|---:|---:|
| 1 | 2 | 1 |
| 4 | 8 | 4 |
| 10 | 20 | 10 |

Read about [peanut butter](https://en.wikipedia.org/wiki/Peanut_butter).

## The numbers

| Species | Penguins weighed | Average body mass (g) |
|---|---:|---:|
| Gentoo | 123 | 5,076 |
| Chinstrap | 68 | 3,733 |
| Adelie | 151 | 3,701 |

## How it was done

The query is in [sql/weight_by_species.sql](sql/weight_by_species.sql). It reads the same data from a public table in BigQuery, groups the penguins by species and averages their body mass.

## The data

[data/penguins.csv](data/penguins.csv): the Palmer penguins, 344 birds on three islands near Palmer Station, Antarctica. Source: [palmerpenguins](https://allisonhorst.github.io/palmerpenguins/), licence CC0 (free to reuse).

## Limits

- Two of the 344 penguins have no body mass, so 342 were averaged.
- The Gentoo penguins were all measured on one island, Biscoe. The data cannot say whether Gentoo penguins elsewhere weigh the same.
- The averages mix males and females, and males are heavier.

  ```mermaid
flowchart LR
    A[Penguin data] --> B[SQL: average by species]
    B --> C[Table of 3 rows]
    C --> D[Bar chart]
```
