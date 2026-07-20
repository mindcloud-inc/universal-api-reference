# Get Card URL with CardClan

Generates a personalized CardClan card URL without sending email.

## Endpoint

- **Method:** `POST`
- **Path:** `/integration/get-card-url`
- **Base URL:** `https://app.cardclan.io/api`
- **Official documentation:** [Get Card URL](https://docs.cardclan.io/api-reference/integration/actions/get-card-url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `card` | body | `string` | yes | Card ID for URL generation. |
| `integrationId` | body | `string` | yes | Integration configuration ID. |
| `mergeTags[]` | body | `array<object>` | yes | Array of merge tag objects with recipient data. |
