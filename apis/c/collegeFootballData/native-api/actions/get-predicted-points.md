# List Predicted Points with College Football Data

Retrieves predicted points by down and distance from College Football Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/ppa/predicted`
- **Base URL:** `https://api.collegefootballdata.com`
- **Official documentation:** [List Predicted Points](https://api.collegefootballdata.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `down` | query | `number` | yes | Down value |
| `distance` | query | `number` | yes | Distance value |
