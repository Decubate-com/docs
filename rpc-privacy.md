---
label: RPC Privacy
layout: default
icon: ":closed_lock_with_key:"
order: 71
---
# Zero-tracking
Decubate shields user data and metadata before requests are relayed to RPC providers. Its lightweight design is able to scale to support high traffic volume. 
While private transactions may still be vulnerable to some form of tracing, Decubate achieves true zero-tracking through a number of technical methods:
![](../static/rpc-diagram.png)

## Metamask masking
Decubate replaces metadata attached to a user’s request with its own. As a result, the original metadata attached to a particular request, and any personal information which identifies the user, is removed from the view of RPC providers.

## Random patching
Requests are dispatched randomly to RPC providers, which makes it impossible to log the association between accounts with the same private key, even when multiple requests are sent from different addresses consecutively.

## Burn after delivery
Decubate does not store or collect data and metadata that passes through the RPC, which are discarded once the request is complete.