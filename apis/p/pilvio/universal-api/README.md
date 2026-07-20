# <img src="https://images.mindcloud.co/apps/icons/pilvio_1776777358905.png" alt="Pilvio logo" width="28" height="28"> Pilvio: Universal API

Cloud infrastructure provider for managing virtual machines, storage, networking, billing resources, and account configuration through the Pilvio REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pilvio/latest
- **Category:** IT Operations / DevOps
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pilvio.com/
- **Vendor API docs:** https://api.pilvio.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Info](actions/get-user-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/get-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### API Keys

| Action | Method | Description |
| --- | --- | --- |
| [Get S3 Keys](actions/get-s3-keys.md) | GET |  |
| [List SSH Keys](actions/list-ssh-keys.md) | GET |  |
| [List Tokens](actions/list-tokens.md) | GET |  |

### Devices

| Action | Method | Description |
| --- | --- | --- |
| [Get VM Info](actions/get-vm-info.md) | GET |  |
| [List VMs](actions/list-vms.md) | GET |  |

### Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Get Floating IP](actions/get-floating-ip.md) | GET |  |
| [Get Load Balancer](actions/get-load-balancer.md) | GET |  |
| [List Floating IPs](actions/list-floating-ips.md) | GET |  |
| [List Load Balancers](actions/list-load-balancers.md) | GET |  |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Get Disk](actions/get-disk.md) | GET |  |
| [Get S3 API Info](actions/get-s3-api-info.md) | GET |  |
| [List Disks](actions/list-disks.md) | GET |  |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Get Bucket](actions/get-bucket.md) | GET |  |
| [List Buckets](actions/list-buckets.md) | GET |  |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [List Locations](actions/list-locations.md) | GET |  |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [Get Billing Account Details](actions/get-billing-account-details.md) | GET |  |
| [List Billing Accounts](actions/list-billing-accounts.md) | GET |  |

### Policies

| Action | Method | Description |
| --- | --- | --- |
| [List Firewalls](actions/list-firewalls.md) | GET |  |

### Resource Allocations

| Action | Method | Description |
| --- | --- | --- |
| [List Billing Account Resources](actions/list-billing-account-resources.md) | GET |  |
| [List VM Resource Pools](actions/list-vm-resource-pools.md) | GET |  |

### Sync States

| Action | Method | Description |
| --- | --- | --- |
| [List Replicas](actions/list-replicas.md) | GET |  |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Network Data](actions/get-network-data.md) | GET |  |
| [Get VM Parameters](actions/get-vm-parameters.md) | GET |  |
| [List App Catalog Images](actions/list-app-catalog-images.md) | GET |  |
| [List Bootable Media Images](actions/list-bootable-media-images.md) | GET |  |
| [List Networks](actions/list-networks.md) | GET |  |
| [List Plain OS Images](actions/list-plain-os-images.md) | GET |  |
| [List VM Images](actions/list-vm-images.md) | GET |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get S3 User](actions/get-s3-user.md) | GET |  |
| [Get User Info](actions/get-user-info.md) | GET |  |

