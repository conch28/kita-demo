# KITA — AGRISENSO Plus demonstration

Five role applications sharing one operating model. Static HTML, no build step,
no server, no database.

| Surface | File |
|---|---|
| Farmer | `Kita_Farmer_App.html` |
| Landbank — lending officer | `LANDBANK_Officer_Workbench.html` |
| Landbank — programme leadership | `LANDBANK_Command_Center.html` |
| Buyer | `Kita_Buyer_App.html` |
| Kita operations | `Kita_Ops_Command.html` |

`index.html` is the launcher.

## The data

Every figure is illustrative. 70 synthetic farmer records against real Philippine
municipalities, real crop economics and real programme terms. No personal data of any
real person appears anywhere.

**No signed buyer offtake agreement is represented.** Buyer relationships sit on a
commitment ladder; the highest rung reached is a conditional demand commitment. No farmer
is shown as financeable on anything below that rung.

State is held in each visitor's own browser. Nothing is shared between visitors and
nothing reaches a server.

## The Operations console is encrypted

`Kita_Ops_Command.html` carries Kita's internal input-margin data — target versus achieved
margin per crop, the margin bridge and the P&L — which does not belong on a public URL in
readable form. It is published as ciphertext: AES-256-GCM, key derived with PBKDF2-SHA256 at
600,000 rounds, decrypted in the visitor's own browser. The passphrase is never transmitted and
the server holds no readable copy.

The other four applications are open.
