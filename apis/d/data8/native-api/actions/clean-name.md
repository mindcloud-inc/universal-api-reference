# Clean Name with Data8

Cleanses a submitted name with Data8.

## Endpoint

- **Method:** `POST`
- **Path:** `/NameCleansing/CleanName.json`
- **Base URL:** `https://webservices.data-8.co.uk`
- **Official documentation:** [Clean Name](https://docs.data-8.co.uk/web-services/namecleansing/cleanname)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `object` | yes | Structured name data to cleanse. |
| `options` | body | `object` | no | Optional settings that control name cleansing behavior. |
