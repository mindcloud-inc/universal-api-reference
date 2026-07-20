# Retrieve Organization Member with Sentry IO

Retrieves an organization member from Sentry IO.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organization_id_or_slug/members/:member_id/`
- **Base URL:** `https://sentry.io/api/0`
- **Official documentation:** [Retrieve Organization Member](https://docs.sentry.io/api/organizations/retrieve-an-organization-member/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id_or_slug` | path | `string` | yes | The Sentry organization ID or slug. |
| `member_id` | path | `string` | yes | The organization member ID. |
