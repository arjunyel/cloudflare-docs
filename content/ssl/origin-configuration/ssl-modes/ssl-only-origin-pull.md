---
pcx_content_type: reference
title: Strict (SSL-Only Origin Pull)
weight: 5
meta:
    title: Strict (SSL-Only Origin Pull) - SSL/TLS encryption modes
---

# Strict (SSL-Only Origin Pull) - SSL/TLS encryption modes

{{<Aside type="note">}}
This method is only available for Enterprise zones.
{{</Aside>}}

Connections to the origin will always be made using SSL/TLS, regardless of the scheme requested by the visitor.

The certificate presented by the origin will be validated the same as with [Full (strict) mode](/ssl/origin-configuration/ssl-modes/full-strict/).

```mermaid
flowchart LR
    accTitle: Strict (SSL-Only Origin Pull) SSL/TLS Encryption
    accDescr: With an encryption mode of Strict (SSL-Only Origin Pull), all connections to the origin will always be made using SSL/TLS.
    A[Browser] <--Encrypted--> B((Cloudflare))<--Encrypted--> C[("Origin server (verified) &#9989;")]
```

## Use when

You want the most secure configuration available for your origin, you are an Enterprise customer, and you meet the requirements for [**Full (strict)** mode](/ssl/origin-configuration/ssl-modes/full-strict/).

## Required setup

The setup is generally the same as [**Full (strict)** mode](/ssl/origin-configuration/ssl-modes/full-strict/), but you select **Strict (SSL-Only Origin Pull)** for your encryption mode.

You also need to enable [Authenticated origin pulls](/ssl/origin-configuration/authenticated-origin-pull/) for this to work.

## Limitations

{{<render file="_ssl-mode-errors.md">}}