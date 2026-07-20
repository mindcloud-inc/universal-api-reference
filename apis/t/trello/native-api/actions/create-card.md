# Create Card with Trello

Creates a new card in Trello.

## Endpoint

- **Method:** `POST`
- **Path:** `cards`
- **Base URL:** `https://api.trello.com/1`
- **Official documentation:** [Create Card](https://developer.atlassian.com/cloud/trello/rest/api-group-cards/#api-cards-post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `desc` | query | `string` | no |
| `due` | query | `string` | no |
| `dueComplete` | query | `boolean` | no |
| `idLabels[]` | query | `array` | no |
| `idList` | query | `string` | yes |
| `idMembers[]` | query | `array` | no |
| `name` | query | `string` | no |
| `pos` | query | `string` | no |
| `start` | query | `string` | no |
| `urlSource` | query | `string` | no |
