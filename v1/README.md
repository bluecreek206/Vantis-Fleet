# VANTIS Fleet API

> **v1.0.0** · 95 Aircraft · Stellar Naming Scheme

Static JSON API for the VANTIS private aviation fleet. Designed for GitHub Pages deployment.

## Overview

The VANTIS Fleet API provides comprehensive data for a fleet of 95 private aircraft spanning four global regions. Each aircraft is assigned a unique stellar name from the astronomical catalog.

## Fleet Summary

| Metric | Value |
|--------|-------|
| Total Aircraft | 95 |
| Active | 68 |
| Maintenance | 9 |
| Charter | 18 |
| Regions | NA (28), EU (25), APAC (24), LATAM (18) |

## Categories

| Category | Count |
|----------|-------|
| ultra-long-range | 32 |
| long-range | 24 |
| super-midsize | 24 |
| light | 15 |

## Endpoints

| Endpoint | Description |
|----------|-------------|
| `/v1/fleet.json` | Complete fleet (95 aircraft) |
| `/v1/fleet-meta.json` | Aggregated fleet metadata |
| `/v1/fleet-regions.json` | Aircraft grouped by region |
| `/v1/fleet-active.json` | Active aircraft only (68) |
| `/v1/schema.json` | JSON Schema (draft-07) |
| `/v1/regions/na.json` | North America (28 aircraft) |
| `/v1/regions/eu.json` | Europe (25 aircraft) |
| `/v1/regions/apac.json` | Asia-Pacific (24 aircraft) |
| `/v1/regions/latam.json` | Latin America (18 aircraft) |

## Aircraft Record

Each aircraft record contains 18 fields:

```json
{
  "id": "vnt-0001",
  "name": "Sirius",
  "registration": "NVNT001",
  "callsign": "VANTIS001",
  "msn": "VNT-0001",
  "type": "Gulfstream G700",
  "category": "ultra-long-range",
  "seats": 19,
  "range_nm": 7500,
  "status": "active",
  "region": "NA",
  "home_base": "KTEB",
  "position": { "lat": 40.8501, "lon": -74.0608 },
  "delivered": "2022-03-15",
  "last_service": "2025-11-08",
  "hours_total": 4520,
  "cycles_total": 1830
}
```

## Naming Scheme

Aircraft are named after prominent stars in the night sky, starting with **Sirius** (vnt-0001) through **Vindemiatrix** (vnt-0095).

## Region Hubs

- **NA**: KTEB, KVNY, KBOS, KFLL, KLAS, KORD, KDAL, KLAX
- **EU**: EGLF, LFPB, EDDR, LSZH, LEMD, EGSS, LIML, ESSA
- **APAC**: VHHH, WSSS, RJTT, YSSY, OMDB, VIDP, ZBAA, RKSI
- **LATAM**: SBGR, SAEZ, MMMX, SKBO, SCEL, SPIM, MROC, TTPP

## Deployment

1. Download `VANTIS_Fleet_API_v1.zip`
2. Extract to your GitHub Pages repository root
3. Enable GitHub Pages in repository settings
4. Access at `https://<username>.github.io/v1/fleet.json`

## Schema Validation

Validate aircraft records against `/v1/schema.json` (JSON Schema draft-07).

## License

MIT License · VANTIS Fleet API · Generated 2026-06-22T05:32:00Z
