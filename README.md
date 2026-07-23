# McFleet

Player stats for McFleet (Minecraft), exported from MongoDB.

## Layout

```
player stats/           # one JSON file per player
  KqTF.json
  ...
top players/
  Top 1/
  Top 10/
  Top 20/
  Top 50/
  Top 100/
```

### top players

Each `Top N` folder contains:

| File | What it is |
|------|------------|
| `leaderboard.json` | Top N players by wins (then final kills, kills) |
| `totals.json` | Sum of all numeric stats for those Top N |
| `by_stat.json` | Top N for every stat + totals |
| `players/` | Individual ranked files (`001_Username.json`, …) |

## Source

`stats` database → `stats` collection → document `_id: "players"`.
