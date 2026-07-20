# List Vulnerabilities with Action1

Retrieves vulnerabilities from Action1 for an organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/vulnerabilities/:orgId`
- **Base URL:** `https://app.action1.com/api/3.0`
- **Official documentation:** [List Vulnerabilities](https://app.action1.com/apidocs/#/Vulnerability%20Management/vulnerabilities_orgId_get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orgId` | path | `string` | yes | Provide an organization ID. |
