# Platform-internal identify — sync dashboard user attributes with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/platform/identify`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Platform-internal identify — sync dashboard user attributes](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Accepted for contract parity but ignored — authenticated user's email is used |
| `firstName` | body | `string` | no | Contact's first name |
| `lastName` | body | `string` | no | Contact's last name |
| `traits` | body | `object` | no | Arbitrary key-value attributes. Keys are automatically prefixed with `md_` before storage. Keys must be alphanumeric with underscores/hyphens. Values must be primitives: string, number, or boolean. Maximum 10 traits per call. |
