# CryptoExchange Log Filter

This project is a Bash script that filters and processes cryptocurrency transaction logs based on various criteria.

## Description

The script `xtf` is used to parse log files and filter transaction data for a specific user. It supports filtering by date and currency, and can display summaries or detailed logs.

## Usage

```
./xtf [-h|--help] [FILTERS] [COMMAND] USER LOG [LOG2 [...]]
```

### Filters

- `-a DATETIME` – Only transactions **after** this date (`YYYY-MM-DD HH:MM:SS`)
- `-b DATETIME` – Only transactions **before** this date
- `-c CURRENCY` – Filter by a specific currency (e.g., BTC, ETH)

### Commands (choose one)

- `list` – List all records for the given user
- `income` – Calculate total income
- `outcome` – Calculate total outcome

## Example

```
./xtf -a "2024-01-01 00:00:00" -c BTC list alice cryptoexchange.log
```

## Files

- `xtf` – Main script
- `*.log` – Sample input log files for testing
