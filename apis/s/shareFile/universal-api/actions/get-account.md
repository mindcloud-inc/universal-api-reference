# ShareFile: Get Account



```
GET https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShareFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/get-account?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/get-account?${params}`, {
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
| `id` | string | yes | The ShareFile account identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "AccountManagerId": "string",
      "AccountSubType": "string",
      "BandwidthMax": 1,
      "BaseDiskSpace": 1,
      "BaseUsers": 1,
      "BillingContactId": "string",
      "BillingRate": 1,
      "BillingType": "string",
      "CanCancel": true,
      "CancellationDate": "string",
      "CanChangeBilling": true,
      "CanChangePlan": true,
      "CanConvertFreeTrial": true,
      "CloudStorageType": "string",
      "CompanyName": "Ava Chen",
      "Country": "string",
      "CreationDate": "string",
      "DiskSpaceMax": 1,
      "Id": "string",
      "IsCancelled": true,
      "IsFreeTrial": true,
      "IsSolutionOffering": true,
      "IsSuspended": true,
      "LastBillingDate": "string",
      "LogoURL": "https://example.com",
      "MasterAdminId": "string",
      "NextBillingDate": "string",
      "odata": {
        "metadata": "string",
        "type": "string"
      },
      "Phone": "string",
      "PlanName": "Ava Chen",
      "PlanTrack": "string",
      "PlanTrackEnum": "string",
      "Subdomain": "string",
      "Subdomains": [
        "string"
      ],
      "TechnicalContactId": "string",
      "url": "https://example.com",
      "UserMax": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AccountManagerId` | string | The account manager user identifier. |
| `AccountSubType` | string | The ShareFile account subtype. |
| `BandwidthMax` | number | The maximum bandwidth allocation. |
| `BaseDiskSpace` | number | The base disk space allocation. |
| `BaseUsers` | number | The included user count. |
| `BillingContactId` | string | The billing contact user identifier. |
| `BillingRate` | number | The current billing rate. |
| `BillingType` | string | The ShareFile billing type. |
| `CanCancel` | boolean | Whether the account can be cancelled. |
| `CancellationDate` | string | The cancellation timestamp. |
| `CanChangeBilling` | boolean | Whether billing can be changed. |
| `CanChangePlan` | boolean | Whether the plan can be changed. |
| `CanConvertFreeTrial` | boolean | Whether the account can convert from free trial. |
| `CloudStorageType` | string | The cloud storage type. |
| `CompanyName` | string | The ShareFile account company name. |
| `Country` | string | The account country. |
| `CreationDate` | string | The account creation timestamp. |
| `DiskSpaceMax` | number | The maximum disk space allocation. |
| `Id` | string | The ShareFile account identifier. |
| `IsCancelled` | boolean | Whether the account is cancelled. |
| `IsFreeTrial` | boolean | Whether the account is a free trial. |
| `IsSolutionOffering` | boolean | Whether the account is a solution offering. |
| `IsSuspended` | boolean | Whether the account is suspended. |
| `LastBillingDate` | string | The last billing date. |
| `LogoURL` | string | The logo URL. |
| `MasterAdminId` | string | The master admin user identifier. |
| `NextBillingDate` | string | The next billing date. |
| `odata.metadata` | string | The OData metadata URL for the returned account. |
| `odata.type` | string | The OData type for the returned account. |
| `Phone` | string | The account phone number. |
| `PlanName` | string | The ShareFile plan name. |
| `PlanTrack` | string | The ShareFile plan track. |
| `PlanTrackEnum` | string | The plan track enum value. |
| `Subdomain` | string | The primary ShareFile subdomain. |
| `Subdomains` | array<string> | The ShareFile subdomains tied to the account. |
| `TechnicalContactId` | string | The technical contact user identifier. |
| `url` | string | The API URL for the returned account. |
| `UserMax` | number | The maximum user count. |

## Native endpoint

Through the native ShareFile API, this operation is `GET /Accounts({{id}})` (base URL `https://{{credentials.accessTokenRequest.subdomain}}.{{credentials.accessTokenRequest.apicp}}/sf/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

