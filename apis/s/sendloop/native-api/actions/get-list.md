# Get List with Sendloop

## Endpoint

- **Method:** `POST`
- **Path:** `/list.get/json`
- **Base URL:** `https://{subdomain}.sendloop.com/api/v3`
- **Official documentation:** [Get List](https://chmyos.notion.site/Get-a-List-cc01af17aac64de9a6fecd9a82359815)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ListID` | body | `number` | yes | ID of the target subscriber list |
| `GetCustomFields` | body | `number` | no | Set to 1 to include the list's created custom fields |
