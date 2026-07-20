# Get People with xMatters

Retrieves people from your xMatters instance.

## Endpoint

- **Method:** `GET`
- **Path:** `people`
- **Base URL:** `https://mindcloud.xmatters.com/api/xm/1`
- **Official documentation:** [Get People](https://help.xmatters.com/xmapi/index.html#get-people)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | query | `string` | no | Limit search to specific fields such as FIRST_NAME or LAST_NAME. |
| `operand` | query | `string` | no | Choose whether the search terms should use AND or OR behavior. |
| `search` | query | `string` | no | Search people by name, web login, email address, or phone number. |
| `status` | query | `string` | no | Filter returned people by account status. |
