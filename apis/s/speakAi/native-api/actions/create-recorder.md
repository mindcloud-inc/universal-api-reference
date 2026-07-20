# Create Recorder with Speak Ai

Creates a recorder in Speak Ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/recorder/create`
- **Base URL:** `https://api.speakai.co/v1`
- **Official documentation:** [Create Recorder](https://docs.speakai.co/#0e1a7b2c-9e8b-4a22-8560-d6f95a86f124)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Display name for the recorder. |
| `description` | body | `string` | no | Optional description for the recorder. |
| `folderId` | body | `string` | no | Optional folder for recordings created by this recorder. |
| `sourceLanguage` | body | `string` | no | Optional source language for recorder submissions. |
| `minDuration` | body | `number` | no | Optional minimum recording length in seconds. |
| `maxDuration` | body | `number` | no | Optional maximum recording length in seconds. |
