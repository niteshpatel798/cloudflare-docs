---
pcx_content_type: reference
title: Delete variants
weight: 6
---

# Delete variants

You can delete variants via the Images dashboard or via API.

{{<Aside type="warning" header="Warning">}}

Deleting a variant is a global action that will affect other images that contain that variant.

{{</Aside>}}

## Delete a variant using the dashboard

1. Log in to the [Cloudflare dashboard](https://dash.cloudflare.com/login) and select your account.
2. Select **Images** > **Variants**.
3. Find the variant you want to remove and select **Delete**.

{{<Aside type="note" header="Note">}}

You cannot delete the public variant.

{{</Aside>}}

## Delete a variant using the API

For detailed information on using the API, refer to the [API endpoint](https://api.cloudflare.com/#cloudflare-images-variants-delete-a-variant) documentation.

The following example deletes a variant through an API call:

```bash
curl -X DELETE https://api.cloudflare.com/client/v4/account/<ACCOUNT_ID>/images/v1/variants/<VARIANT_NAME> \
--header 'Authorization: Bearer <API_TOKEN>'
```

You will receive a response similar to this:

```json
{
  "result": {},
  "success": true,
  "errors": [],
  "messages": []
}
```