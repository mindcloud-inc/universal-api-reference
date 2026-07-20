# Upsert Subscriber with Realcrux

## Endpoint

- **Method:** `POST`
- **Path:** `subscribers`
- **Base URL:** `https://sendcrux.com/api/v1`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_uid` | body | `string` | yes | UID of the Sendcrux mail list that should receive or update the subscriber. |
| `EMAIL` | body | `string` | yes | Email address of the subscriber. The verified list contract marks EMAIL as required. |
| `FIRST_NAME` | body | `string` | no | First name field exposed by the verified Sendcrux list. |
| `LAST_NAME` | body | `string` | no | Last name field exposed by the verified Sendcrux list. |
| `COUNTRY` | body | `string` | no | Country field exposed by the verified Sendcrux list. |
| `PHONE_NUMBER` | body | `string` | no | Phone number field exposed by the verified Sendcrux list. |
| `COMPANY` | body | `string` | no | Company field exposed by the verified Sendcrux list. |
