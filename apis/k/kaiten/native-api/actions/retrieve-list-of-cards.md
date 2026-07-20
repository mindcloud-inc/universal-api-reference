# Retrieve List of Cards with Kaiten

Retrieves cards from Kaiten.

## Endpoint

- **Method:** `GET`
- **Path:** `/cards`
- **Base URL:** `https://{companyDomain}.kaiten.ru/api/latest`
- **Official documentation:** [Retrieve List of Cards](https://developers.kaiten.ru/cards/get-list-of-cards)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board_id` | query | `number` | no | Filter cards by board ID. |
