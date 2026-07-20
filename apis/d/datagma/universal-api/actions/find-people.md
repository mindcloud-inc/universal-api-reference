# Datagma: Find People

Finds people in Datagma by company and job title.

```
GET https://connect.mindcloud.co/v1/universal/datagma/latest/actions/find-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datagma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datagma/latest/actions/find-people?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datagma/latest/actions/find-people?${params}`, {
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
| `current_job_title` | string | no | Job title or title pattern to search for within the target company. |
| `domain` | string | no | Company domain used as the company input. |
| `countries` | string | no | Country filter in minimal letters, if you want to narrow the result set. |
| `fuzzy` | string | no | Set to true to broaden matching beyond exact job-title matches. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "employees": [
        {}
      ],
      "listOfInvalidDataInput": [
        "string"
      ],
      "listOfValidLinkedInId": [
        "https://example.com"
      ],
      "transferData": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `employees` | array<object> |  |
| `listOfInvalidDataInput` | array<string> |  |
| `listOfValidLinkedInId` | array<string> |  |
| `transferData` | array<object> |  |

## Native endpoint

Through the native Datagma API, this operation is `GET /v1/find_people` (base URL `https://gateway.datagma.net/api/ingress`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-people.md) for the provider-specific parameters and requirements.

