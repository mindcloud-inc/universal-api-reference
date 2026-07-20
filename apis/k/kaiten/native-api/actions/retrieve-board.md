# Retrieve Board with Kaiten

Retrieves a board from Kaiten.

## Endpoint

- **Method:** `GET`
- **Path:** `/spaces/:spaceId/boards/:boardId`
- **Base URL:** `https://{companyDomain}.kaiten.ru/api/latest`
- **Official documentation:** [Retrieve Board](https://developers.kaiten.ru/space-boards/get-board)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spaceId` | path | `number` | yes | The Kaiten space ID. |
| `boardId` | path | `number` | yes | The Kaiten board ID. |
