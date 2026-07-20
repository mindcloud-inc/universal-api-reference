# Create Domain with Resend

Creates a new domain in Resend.

## Endpoint

- **Method:** `POST`
- **Path:** `/domains`
- **Base URL:** `https://api.resend.com`
- **Official documentation:** [Create Domain](https://resend.com/docs/api-reference/domains/create-domain)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `capabilities.sending` | body | `string` | no | — |
| `name` | body | `string` | yes | The name of the domain you want to create. |
| `capabilities.receiving` | body | `string` | no | — |
| `region` | body | `string` | no | Region where emails will be sent from. Possible values: us-east-1, eu-west-1, sa-east-1, ap-northeast-1. |
| `custom_return_path` | body | `string` | no | Subdomain used for Return-Path address (SPF/DMARC/bounces). Defaults to send. |
| `open_tracking` | body | `boolean` | no | Track the open rate of each email. |
| `click_tracking` | body | `boolean` | no | Track clicks within each HTML email. |
| `tls` | body | `string` | no | TLS mode. Possible values: opportunistic or enforced. |
| `capabilities` | body | `object` | no | Domain capabilities object. Include sending (enabled\|disabled) and receiving (enabled\|disabled). At least one capability should be enabled. |
