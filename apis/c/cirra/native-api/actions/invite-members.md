# Invite Members with Cirra

Invites members to the authenticated Cirra company.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/members`
- **Base URL:** `http://api-public:9801`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails` | body | `string` | yes | Send multiple values as a array. |
