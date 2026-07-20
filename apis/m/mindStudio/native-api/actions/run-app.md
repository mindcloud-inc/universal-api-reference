# Run App with MindStudio

Runs an app in MindStudio.

## Endpoint

- **Method:** `POST`
- **Path:** `/apps/run`
- **Base URL:** `https://api.mindstudio.ai/developer/v2`
- **Official documentation:** [Run App](https://university.mindstudio.ai/docs/developers/api-reference#run-an-app)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | body | `string` | yes | The MindStudio app ID to run. |
| `variables` | body | `object` | no | Variables to pass into the MindStudio app run. |
| `workflow` | body | `string` | no | Optional workflow to run within the app. |
| `callbackUrl` | body | `string` | no | Optional callback URL for asynchronous app runs. |
| `includeBillingCost` | body | `boolean` | no | Whether to include billing cost information in the response. |
