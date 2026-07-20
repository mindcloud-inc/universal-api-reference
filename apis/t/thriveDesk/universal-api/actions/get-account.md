# ThriveDesk: Get Account



```
GET https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ThriveDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/get-account?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "company": {},
      "had_onboarding_survey": true,
      "inboxes": [
        "string"
      ],
      "onboarding": {},
      "organizations": [
        {}
      ],
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | object | Company/account details. |
| `had_onboarding_survey` | boolean | Whether onboarding survey was completed. |
| `inboxes` | array<string> | Inbox IDs available to the current user. |
| `onboarding` | object | Onboarding completion flags. |
| `organizations` | array<object> | Organizations available to the current user. |
| `user` | object | Current user details. |

## Native endpoint

Through the native ThriveDesk API, this operation is `GET /v1/me` (base URL `https://api.thrivedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

