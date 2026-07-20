# Membership Generate Cart with Explara

Retrieves a membership cart calculation from Explara.

## Endpoint

- **Method:** `POST`
- **Path:** `/cm/api/membership/generate-cart`
- **Base URL:** `https://www.explara.com`
- **Official documentation:** [Membership Generate Cart](https://apidocs.explara.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | body | `string` | yes | Explara group identifier. |
| `membership[]` | body | `array<object>` | yes | Array of membership selection objects. |
