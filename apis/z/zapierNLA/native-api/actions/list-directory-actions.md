# List Directory Actions with Zapier NLA

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/search/actions/`
- **Base URL:** `https://actions.zapier.com`
- **Official documentation:** [List Directory Actions](https://nla.zapier.com/api/v1/dynamic/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | Search term for directory actions. |
| `include_exposed` | query | `boolean` | no | Include actions currently exposed by the Zapier account. |
| `count` | query | `number` | no | Maximum number of directory actions to return. |
