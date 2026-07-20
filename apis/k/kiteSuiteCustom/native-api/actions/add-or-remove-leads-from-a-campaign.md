# Add or remove leads from a campaign with Kite Suite

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/campaign/lead`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Add or remove leads from a campaign](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `campaign` | body | `string` | yes | The ID of the campaign. |
| `leads[]` | body | `array` | yes | Array of lead IDs to add or remove. |
| `action` | body | `string` | yes | The action to perform ("add" or "remove"). |
