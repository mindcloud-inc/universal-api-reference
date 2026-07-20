# List Forms with RapidoForm

Retrieves all available forms from RapidoForm.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/surveys`
- **Base URL:** `https://www.rapidoform.com/be`
- **Official documentation:** [List Forms](https://www.rapidoform.com/developers/docs/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number to retrieve. |
| `surveyId` | query | `string` | no | — |
| `status` | query | `string` | no | Only return forms with the selected status. |
