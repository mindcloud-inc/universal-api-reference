# TestDome: Get Current Plan

Retrieves the current plan from TestDome.

```
GET https://connect.mindcloud.co/v1/universal/testDome/latest/actions/get-current-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TestDome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testDome/latest/actions/get-current-plan?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/testDome/latest/actions/get-current-plan?${params}`, {
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
      "_links": {},
      "canCloneQuestions": {},
      "canCreateTest": {},
      "id": 1,
      "isPaymentSubscriptionActive": true,
      "isSubscription": true,
      "isTrial": true,
      "name": "Ava Chen",
      "questionsToCloneAvailable": 1,
      "supportsPremiumFeatures": {},
      "supportsSso": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | object | Dictionary |
| `canCloneQuestions` | object | If PlanAuthorizationModel.Authorized = `true`, this account can clone questions. If PlanAuthorizationModel.Authorized = `false`, the PlanAuthorizationModel.ErrorMessage property will be filled with information of why the authorization failed. |
| `canCreateTest` | object | If PlanAuthorizationModel.Authorized = `true`, the plan allows the user to create tests. If PlanAuthorizationModel.Authorized = `false`, the PlanAuthorizationModel.ErrorMessage property will be filled with information of why the authorization failed. |
| `id` | number | The plan ID. |
| `isPaymentSubscriptionActive` | boolean | Indicates if the plan has an active payment method set up. |
| `isSubscription` | boolean | Indicates if the plan is a recurring subscription. |
| `isTrial` | boolean | Indicates if the plan is a trial. |
| `name` | string | The plan name. |
| `questionsToCloneAvailable` | number | The remaining number of questions that can be cloned this month. |
| `supportsPremiumFeatures` | object | If PlanAuthorizationModel.Authorized = `true`, this account supports premium features. This flag does not indicate if the plan is paid. If PlanAuthorizationModel.Authorized = `false`, the PlanAuthorizationModel.ErrorMessage property will be filled with information of why the authorization failed. For example, it can be a trial plan, which is not paid but allows users to see premium questions and take advantage of other premium features. |
| `supportsSso` | object | If PlanAuthorizationModel.Authorized = `true`, this account supports SSO. If PlanAuthorizationModel.Authorized = `false`, the PlanAuthorizationModel.ErrorMessage property will be filled with information of why the authorization failed. |
| `type` | string | The plan type. |

## Native endpoint

Through the native TestDome API, this operation is `GET /accounts/current/plan` (base URL `https://api.staging.testdome.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-plan.md) for the provider-specific parameters and requirements.

