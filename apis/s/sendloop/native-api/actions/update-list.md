# Update List with Sendloop

## Endpoint

- **Method:** `POST`
- **Path:** `/list.update/json`
- **Base URL:** `https://{subdomain}.sendloop.com/api/v3`
- **Official documentation:** [Update List](https://chmyos.notion.site/Update-a-List-71043bfda0394f2fa129cf24c7453512)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ListID` | body | `number` | yes | ID number of the target subscriber list |
| `Name` | body | `string` | no | Name of the list |
| `OptInMode` | body | `string` | no | Pass Single or Double |
