# Pilvio: Native API Reference

A consolidated summary of Pilvio's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://api.pilvio.com/
- **API base URL:** `https://api.pilvio.com/v1`

## Authentication

### API Key

Use a Pilvio API token in the apikey request header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
apikey: <apiKey>
```

[Official authentication documentation](https://api.pilvio.com/#authentication)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Billing Account Details](actions/get-billing-account-details.md) | `GET /payment/billing_account` | [docs](https://api.pilvio.com/#billing-account-details) |
| [Get Bucket](actions/get-bucket.md) | `GET /storage/bucket` | [docs](https://api.pilvio.com/#get-bucket) |
| [Get Disk](actions/get-disk.md) | `GET /storage/disks/{disk_uuid}` | [docs](https://api.pilvio.com/#get-disk) |
| [Get Floating IP](actions/get-floating-ip.md) | `GET /network/ip_addresses/{public_ipv4_address}` | [docs](https://api.pilvio.com/#get-floating-ip) |
| [Get Load Balancer](actions/get-load-balancer.md) | `GET /network/load_balancers/{load_balancer_uuid}` | [docs](https://api.pilvio.com/#get-user-load-balancer-by-uuid) |
| [Get Network Data](actions/get-network-data.md) | `GET /network/network/{network_uuid}` | [docs](https://api.pilvio.com/#get-network-data) |
| [Get S3 API Info](actions/get-s3-api-info.md) | `GET /storage/api/s3` | [docs](https://api.pilvio.com/#s3-api-info) |
| [Get S3 Keys](actions/get-s3-keys.md) | `GET /storage/user/keys` | [docs](https://api.pilvio.com/#get-keys) |
| [Get S3 User](actions/get-s3-user.md) | `GET /storage/user` | [docs](https://api.pilvio.com/#get-s3-user) |
| [Get User Info](actions/get-user-info.md) | `GET /user-resource/user` | [docs](https://api.pilvio.com/#get-user-info) |
| [Get VM Info](actions/get-vm-info.md) | `GET /user-resource/vm` | [docs](https://api.pilvio.com/#get-vm-info) |
| [Get VM Parameters](actions/get-vm-parameters.md) | `GET /api/parameters/vm` | [docs](https://api.pilvio.com/#vm-parameters) |
| [List App Catalog Images](actions/list-app-catalog-images.md) | `GET /config/vm_images/app_catalog` | [docs](https://api.pilvio.com/#get-app-catalog-images) |
| [List Billing Account Resources](actions/list-billing-account-resources.md) | `GET /user-resource/billing_resources` | [docs](https://api.pilvio.com/#list-billing-account-39-s-resources) |
| [List Billing Accounts](actions/list-billing-accounts.md) | `GET /payment/billing_account/list` | [docs](https://api.pilvio.com/#list-billing-accounts) |
| [List Bootable Media Images](actions/list-bootable-media-images.md) | `GET /config/boot_images` | [docs](https://api.pilvio.com/#list-bootable-media-images) |
| [List Buckets](actions/list-buckets.md) | `GET /storage/bucket/list` | [docs](https://api.pilvio.com/#list-buckets) |
| [List Disks](actions/list-disks.md) | `GET /storage/disks` | [docs](https://api.pilvio.com/#list-disks) |
| [List Firewalls](actions/list-firewalls.md) | `GET /network/firewalls` | [docs](https://api.pilvio.com/#list-firewalls) |
| [List Floating IPs](actions/list-floating-ips.md) | `GET /network/ip_addresses` | [docs](https://api.pilvio.com/#list-floating-ips) |
| [List Load Balancers](actions/list-load-balancers.md) | `GET /network/load_balancers` | [docs](https://api.pilvio.com/#list-user-load-balancers) |
| [List Locations](actions/list-locations.md) | `GET /config/locations` | [docs](https://api.pilvio.com/#list-locations) |
| [List Networks](actions/list-networks.md) | `GET /network/networks` | [docs](https://api.pilvio.com/#list-networks) |
| [List Plain OS Images](actions/list-plain-os-images.md) | `GET /config/vm_images/plain_os` | [docs](https://api.pilvio.com/#get-plain-os-images) |
| [List Replicas](actions/list-replicas.md) | `GET /user-resource/vm/replica` | [docs](https://api.pilvio.com/#list-replicas) |
| [List SSH Keys](actions/list-ssh-keys.md) | `GET /user-resource/ssh_keys` | [docs](https://api.pilvio.com/#list-ssh-keys) |
| [List Tokens](actions/list-tokens.md) | `GET /user-resource/token/list` | [docs](https://api.pilvio.com/#list-tokens) |
| [List VM Images](actions/list-vm-images.md) | `GET /config/vm_images` | [docs](https://api.pilvio.com/#vm-images-list) |
| [List VM Resource Pools](actions/list-vm-resource-pools.md) | `GET /user-resource/host_pool/list` | [docs](https://api.pilvio.com/#list-vm-resource-pools) |
| [List VMs](actions/list-vms.md) | `GET /user-resource/vm/list` | [docs](https://api.pilvio.com/#list-vms) |
