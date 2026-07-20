# Disconnect Registered User Connector with Merge Agent Handler

Disconnects a registered user's connector in Merge Agent Handler.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/credentials/registered-users/:registered_user_id/connectors/:connector_slug/`
- **Base URL:** `https://ah-api.merge.dev/api/v1`
- **Official documentation:** [Disconnect Registered User Connector](https://docs.merge.dev/merge-agent-handler/agent-handler/credentials/registered-users-connectors-destroy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `connector_slug` | path | `string` | no | Slug of the connector. |
| `registered_user_id` | path | `string` | no | ID of the registered user. |
