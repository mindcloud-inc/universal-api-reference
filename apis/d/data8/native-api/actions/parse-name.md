# Parse Name with Data8

Parses a submitted name with Data8.

## Endpoint

- **Method:** `POST`
- **Path:** `/NameCleansing/ParseName.json`
- **Base URL:** `https://webservices.data-8.co.uk`
- **Official documentation:** [Parse Name](https://docs.data-8.co.uk/web-services/namecleansing/parsename)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name string to parse. |
| `options` | body | `object` | no | Optional settings that control name parsing behavior. |
