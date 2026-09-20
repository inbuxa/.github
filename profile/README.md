# INBUXA

A complete mail system you run yourself — server, webmail and administration,
installed and versioned together. **Every feature ships under the AGPL**: there
is no paid tier, no license key, and no edition check anywhere in the code.

Built by **[Coffey Labs](https://github.com/Coffey-Labs)**. INBUXA has an
organization of its own because it is three repositories that ship as one
thing, and they belong next to each other — not because it is a separate
shop. The rest of the lab's work, ihasmail included, is over there.

🌐 [inbuxa.org](https://inbuxa.org) &nbsp;·&nbsp; [coffeylabs.org](https://coffeylabs.org) &nbsp;·&nbsp; [@Coffey-Labs](https://github.com/Coffey-Labs)

---

## Projects

### 📮 [inbuxa-server](https://github.com/inbuxa/inbuxa-server) &nbsp;·&nbsp; Rust &nbsp;·&nbsp; AGPL-3.0-only

**The mail server.** JMAP, IMAP, POP3, SMTP, CalDAV, CardDAV, WebDAV and
Sieve, with the spam and DMARC handling, queue management and clustering of a
server meant to carry real mail.

Nine further capabilities, each rebuilt from a written specification and
shipped under the same license as the rest: tenants with their own
domains, administrators and quotas; per-sender masked addresses; deleted mail
held and restorable; operator branding and message templates; an optional
local model as one spam signal; stored metrics and traces with live tracing
and threshold alerts; SCIM 2.0 provisioning from an identity provider; SQL
read replicas with sharded blob and in-memory stores; and per-domain
directories, so a domain can authenticate against its own LDAP, SQL or OIDC.

Two ways in: a fresh installation, or a migration that moves an existing
Stalwart server across — accounts, passwords, aliases, tenants, DNS records,
certificates and mail — with nothing re-entered and nothing re-issued.

### 🛠 [inbuxa-admin](https://github.com/inbuxa/inbuxa-admin) &nbsp;·&nbsp; TypeScript &nbsp;·&nbsp; AGPL-3.0-only

**Full server administration, off the mail host.** Accounts, domains, tenants,
roles and OAuth clients; listeners, certificates and DNS; queues, reports,
tracing and metrics; first-boot setup and recovery.

It talks to the server over JMAP and OAuth like any other client, so it runs
beside the server or on another machine entirely. The mail host itself serves
no web interface.

### 📬 [ihasmail-inbuxa](https://github.com/inbuxa/ihasmail-inbuxa) &nbsp;·&nbsp; TypeScript &nbsp;·&nbsp; AGPL-3.0-only

**The webmail.** A JMAP-only single-page client — mail, calendars, contacts,
files and Sieve filters — in a disposable container that keeps nothing
durable of its own.

The INBUXA-specific fork of [ihasmail](https://github.com/Coffey-Labs/ihasmail),
which continues on its own as a general client.

### 🌐 [inbuxa.org](https://inbuxa.org) &nbsp;·&nbsp; the site

**Where the suite is introduced, documented and downloaded.** `inbuxa.com`,
`inbuxa.net` and the `www.` names redirect to it.

Its repository stays private: it is the site's deployment, not part of the
product, and nothing in it is needed to run or build INBUXA.

---

## Licensing

| Project | License |
|---|---|
| inbuxa-server | AGPL-3.0-only |
| inbuxa-admin | AGPL-3.0-only |
| ihasmail-inbuxa | AGPL-3.0-or-later |

Copyleft without exception — no open-core carve-outs, no source-available
licenses, no relicensed "enterprise" tier. Running INBUXA means its users are
offered its source, which is the point of choosing this license rather than a
permissive one.

## Provenance

inbuxa-server is a fork of Stalwart, copyright © Stalwart Labs LLC, taken
under the AGPL-3.0-only half of its dual license, with upstream's copyright
notices kept on every file they cover. inbuxa-admin is a fork of Stalwart's
web interface on the same terms. A few upstream files carry code from other
projects under MIT or BSD licenses, reproduced with their notices in each
repository's `THIRD-PARTY.md`.

Stalwart is a trademark of Stalwart Labs LLC. INBUXA is not affiliated with or
endorsed by them.

ihasmail-inbuxa is a fork of [ihasmail](https://github.com/Coffey-Labs/ihasmail),
which is Coffey Labs' own and keeps its AGPL-3.0-or-later terms here.
