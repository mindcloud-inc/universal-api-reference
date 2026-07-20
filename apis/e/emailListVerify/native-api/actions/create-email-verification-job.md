# Create Email Verification Job with EmailListVerify

Creates an asynchronous email verification job in EmailListVerify.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/emailJobs`
- **Base URL:** `https://api.emaillistverify.com`
- **Official documentation:** [Create Email Verification Job](https://api.emaillistverify.com/api-doc#/Verification%20Endpoints/createEmailJob)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address to verify asynchronously. |
| `quality` | body | `string` | no | Verification quality. Standard costs 1 credit; high costs 2 credits and can take longer. Accepted values: `0`, `1`. |
