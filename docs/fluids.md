# Fluids

## Production chain

A pumpjack extracts crude oil. The **refinery** (10 crude + 40 FE → 6 diesel + 4 gasoline), **lubricator** (10 crude + 40 FE → 5 lubricant) and **cracker** (10 crude + 40 FE → 8 naphtha) process it.

## Storage and transport

- **Tank (5000 mB)** and **barrel (5000 mB, keeps fluid on break).**
- Pipe output is valved: `tank(x) + filtered_pipe(x)` — flows only on filter match.
- Filtered pipe filters are set with a bucket, cycled with sneak-right-click.

## Uses

- Diesel: diesel furnace fuel. Gasoline: miner fuel.
- Lubricant: 10 items per bucket in vanilla furnaces, weak diesel-furnace fuel, ×1.5 machine boost from 1000 mB.
- Naphtha: becomes plastic pellets and sheets in the molding press.
