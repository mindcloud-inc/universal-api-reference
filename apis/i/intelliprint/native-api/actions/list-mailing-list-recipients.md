# List Mailing List Recipients with Intelliprint

## Endpoint

- **Method:** `GET`
- **Path:** `/mailing_lists/:mailingList/recipients`
- **Base URL:** `https://api.intelliprint.net/v1`
- **Official documentation:** [List Mailing List Recipients](https://docs.intelliprint.net/api)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mailing_list` | path | `string` | yes | The Intelliprint mailing list ID. |
