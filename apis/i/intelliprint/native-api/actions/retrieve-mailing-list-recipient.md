# Retrieve Mailing List Recipient with Intelliprint

## Endpoint

- **Method:** `GET`
- **Path:** `/mailing_lists/:mailingList/recipients/:id`
- **Base URL:** `https://api.intelliprint.net/v1`
- **Official documentation:** [Retrieve Mailing List Recipient](https://docs.intelliprint.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Intelliprint mailing list recipient ID. |
| `mailing_list` | path | `string` | yes | The Intelliprint mailing list ID. |
