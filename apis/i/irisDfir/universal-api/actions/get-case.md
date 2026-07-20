# Iris Dfir: Get Case



```
GET https://connect.mindcloud.co/v1/universal/irisDfir/latest/actions/get-case
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Iris Dfir `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/irisDfir/latest/actions/get-case?connectionId=$CONNECTION_ID&caseIdentifier=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "caseIdentifier": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/irisDfir/latest/actions/get-case?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `caseIdentifier` | number | yes | IRIS case identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "case_customer_id": 1,
      "case_description": "string",
      "case_id": 1,
      "case_name": "Ava Chen",
      "case_soc_id": "string",
      "case_uuid": "string",
      "close_date": "2026-05-07T12:00:00.000Z",
      "closing_note": "string",
      "custom_attributes": {},
      "modification_history": {},
      "open_date": "2026-05-07T12:00:00.000Z",
      "owner": {
        "id": 1,
        "user_email": "ava@example.com",
        "user_login": "string",
        "user_name": "Ava Chen"
      },
      "severity_id": 1,
      "state": {
        "protected": true,
        "state_description": "string",
        "state_id": 1,
        "state_name": "Ava Chen"
      },
      "status_id": 1,
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `case_customer_id` | number |  |
| `case_description` | string |  |
| `case_id` | number |  |
| `case_name` | string |  |
| `case_soc_id` | string |  |
| `case_uuid` | string |  |
| `close_date` | date |  |
| `closing_note` | string |  |
| `custom_attributes` | object |  |
| `modification_history` | object |  |
| `open_date` | date |  |
| `owner.id` | number |  |
| `owner.user_email` | string |  |
| `owner.user_login` | string |  |
| `owner.user_name` | string |  |
| `severity_id` | number |  |
| `state.protected` | boolean |  |
| `state.state_description` | string |  |
| `state.state_id` | number |  |
| `state.state_name` | string |  |
| `status_id` | number |  |
| `user_id` | number |  |

## Native endpoint

Through the native Iris Dfir API, this operation is `GET /api/v2/cases/:case_identifier` (base URL `https://v200.beta.dfir-iris.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-case.md) for the provider-specific parameters and requirements.

