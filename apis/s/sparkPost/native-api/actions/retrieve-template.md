# Retrieve Template with SparkPost

## Endpoint

- **Method:** `GET`
- **Path:** `/templates/:id`
- **Base URL:** `https://api.sparkpost.com/api/v1`
- **Official documentation:** [Retrieve Template](https://developers.sparkpost.com/api/templates/#templates-get-retrieve-a-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `draft` | query | `boolean` | no | Whether to retrieve the draft version. |
| `id` | path | `string` | yes | Template identifier. |
