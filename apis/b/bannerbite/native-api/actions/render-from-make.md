# Render From Make with Bannerbite

Creates a Make render job in Bannerbite.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/integromat/render`
- **Base URL:** `https://api.bannerbite.com`
- **Official documentation:** [Render From Make](https://developer.bannerbite.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobs` | body | `object<object>` | yes | Single Bannerbite Make render job object. Live tenant validation shows this endpoint accepts one object body for a successful render request. |
