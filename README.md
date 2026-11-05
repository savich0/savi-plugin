# Savi Firm — client intake plugin

Bring a legal matter to Savi Firm from your own Claude.

The plugin runs the firm's intake interview in your conversation: it asks what
an attorney needs to start, asks for the documents that already hold the
answers (your charter, cap table, term sheet and so on), and sends what it
gathered to the Savi Firm attorney for that kind of matter.

## Install (Claude Code)

```
/plugin marketplace add savich0/savi-plugin
/plugin install savi-intake@savi-client
```

Then ask for Savi Firm's help, or describe what you need.

## Connecting to the firm

The plugin talks to the firm's server. If the firm gave you an address or a
token, set them before starting Claude:

```bash
export SAVI_MCP_URL="https://<address the firm gave you>/mcp"
export SAVI_MCP_TOKEN="<token the firm gave you>"
```

## What is sent, and what is not

- Sent to the firm: your name and email, a summary of the matter, the facts you
  gave or that were read from your documents (with where each came from), and
  the list of documents read.
- Not sent: the attachments themselves. They stay in your conversation; the
  attorney may ask you for the originals.
- Never sent: Social Security numbers, bank details or passwords.

Using this plugin does not create an attorney-client relationship, and nothing
in it is legal advice. A relationship begins only when Savi Firm clears
conflicts and both sides sign an engagement letter. What you type is not
privileged until then.
