# Create new release with Kite Suite

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/release`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Create new release](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `title` | body | `string` | yes | — |
| `description` | body | `string` | yes | — |
| `startDate` | body | `string` | yes | — |
| `releaseDate` | body | `string` | yes | — |
| `projectID` | body | `string` | yes | — |
| `manager` | body | `string` | yes | — |
