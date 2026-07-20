# Sign In with KIS

Signs in to the KIS API.

## Endpoint

- **Method:** `POST`
- **Path:** `/api_access_auth/sign_in`
- **Base URL:** `https://api.getkis.io/api/v1`
- **Official documentation:** [Sign In](https://doc.getkis.io/documentation/documentation-api/authentification/sauthentifier-a-lapi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_token` | body | `string` | yes | KIS app token from the connection. |
