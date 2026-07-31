# Get Daily Horoscope with Horoscope

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/get-horoscope/daily`
- **Base URL:** `https://freehoroscopeapi.com`
- **Official documentation:** [Get Daily Horoscope](https://freehoroscopeapi.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sign` | query | `list<string>` | yes | Required zodiac sign: aries through pisces. Accepted values: `aquarius`, `aries`, `cancer`, `capricorn`, `gemini`, `leo`, `libra`, `pisces`, `sagittarius`, `scorpio`, `taurus`, `virgo`. |
