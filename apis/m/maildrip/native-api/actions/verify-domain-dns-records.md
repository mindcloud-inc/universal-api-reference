# Verify domain DNS records with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/mumara/sending-domains/{domainId}/verify`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Verify domain DNS records](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domainId` | path | `string` | yes | Domain ID (DynamoDB UUID) |
