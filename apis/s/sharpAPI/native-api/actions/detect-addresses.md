# Detect Addresses with SharpAPI

Creates an address detection job in SharpAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/content/detect_address`
- **Base URL:** `https://sharpapi.com/api/v1`
- **Official documentation:** [Detect Addresses](https://sharpapi.com/en/catalog/ai/content-marketing-automation/address-detector)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | Provide the content from where address information needs to be detected. |
