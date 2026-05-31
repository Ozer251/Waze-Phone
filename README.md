# Waze Phone

Remote policy dashboard for the Waze Lock Manager Android Device Owner app.

## Pages setup

In GitHub, open:

```text
Settings -> Pages
```

Set:

```text
Source: Deploy from a branch
Branch: main
Folder: /docs
```

Then save.

Your dashboard and phone policy URL should be:

```text
https://Ozer251.github.io/Waze-Phone/
https://Ozer251.github.io/Waze-Phone/policy.json
```

Paste the `policy.json` URL into the Android app.

## Remote policy modes

Maintenance mode:

```json
{
  "mode": "maintenance",
  "privateDns": "9t1y9sakh9.cloudflare-gateway.com",
  "hardDisableAdb": false,
  "hardDisableReset": false,
  "extraBlockedPackages": []
}
```

Lockdown mode:

```json
{
  "mode": "lockdown",
  "privateDns": "9t1y9sakh9.cloudflare-gateway.com",
  "hardDisableAdb": false,
  "hardDisableReset": false,
  "extraBlockedPackages": []
}
```

Keep `hardDisableAdb` and `hardDisableReset` false while testing.

## Dashboard GitHub token

The dashboard can publish changes to `docs/policy.json` if you create a fine-grained GitHub token with Contents read/write permission for this repo only. The token is stored only in your browser localStorage. Do not put it in `policy.json`.
