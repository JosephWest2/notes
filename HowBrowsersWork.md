# How Browsers Work
[reference](https://developer.mozilla.org/en-US/docs/Web/Performance/How_browsers_work)

## First Steps

1. DNS Lookup
2. TCP Handshake
3. TLS Negotiation

## Critical Rendering Path

1. DOM Tree built

Preload Scanner scans for and requests high priority resources such as CSS javascript and web fonts

2. CSSOM Tree built

Meanwhile javascript files are parsed compiled and interpreted. Accessibility tree is built.

### Rendering

3. Styles: DOM and CSSOM combined into a render tree.

4. Layout: node geometry is calculated.

5. Paint: Nodes are painted to the screen.

Interactivity is now added and defered javascript is loaded.
