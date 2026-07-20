# List Feed Trainers with NewsBlur

Retrieves feed classifiers from NewsBlur.

## Endpoint

- **Method:** `GET`
- **Path:** `/reader/feeds_trainer`
- **Base URL:** `https://www.newsblur.com`
- **Official documentation:** [List Feed Trainers](https://newsblur.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `feed_id` | query | `number` | no | Optional feed ID to load classifiers for a single feed. |
