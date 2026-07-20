# UpGuard: Get Onboarding Request

Retrieves an onboarding request from UpGuard.

```
GET https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/get-onboarding-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UpGuard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/get-onboarding-request?connectionId=$CONNECTION_ID&onboardingRequestId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "onboardingRequestId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/get-onboarding-request?${params}`, {
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
| `onboardingRequestId` | number | yes | The ID of the onboarding request to retrieve. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native UpGuard API returns.

## Native endpoint

Through the native UpGuard API, this operation is `GET /onboarding_request` (base URL `https://cyber-risk.upguard.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-onboarding-request.md) for the provider-specific parameters and requirements.

