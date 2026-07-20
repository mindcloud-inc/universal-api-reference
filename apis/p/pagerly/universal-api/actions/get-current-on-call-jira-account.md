# Pagerly: Get Current On-Call Jira Account

Retrieves the current on-call Jira account from Pagerly.

```
GET https://connect.mindcloud.co/v1/universal/pagerly/latest/actions/get-current-on-call-jira-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pagerly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pagerly/latest/actions/get-current-on-call-jira-account?connectionId=$CONNECTION_ID&teamName=Select%20a%20Pagerly%20team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamName": "Select a Pagerly team"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pagerly/latest/actions/get-current-on-call-jira-account?${params}`, {
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
| `teamName` | string | yes | Exact Pagerly team name to resolve to a Jira accountId. Example: `Select a Pagerly team`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string | Jira account id for the current on-call user. |

## Native endpoint

Through the native Pagerly API, this operation is `GET /o/currentusersforjira` (base URL `https://api.pagerly.io/pagerly`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-on-call-jira-account.md) for the provider-specific parameters and requirements.

