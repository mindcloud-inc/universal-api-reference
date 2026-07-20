# Retrieve Recipient List with SparkPost

## Endpoint

- **Method:** `GET`
- **Path:** `/recipient-lists/:id`
- **Base URL:** `https://api.sparkpost.com/api/v1`
- **Official documentation:** [Retrieve Recipient List](https://developers.sparkpost.com/api/recipient-lists/#recipient-lists-get-retrieve-a-recipient-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Recipient list identifier. |
| `show_recipients` | query | `boolean` | no | Whether to include recipient records in the response. |
