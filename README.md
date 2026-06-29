Microsoft Fabric — Notebooks & Resources

A growing collection of free, reusable resources for working with Microsoft Fabric — notebooks, templates, and patterns you can drop straight into a workspace and run.

Everything here is MIT-licensed, self-contained (no external dependencies beyond a default Fabric Spark runtime), and built to be useful on day one.

What's in here

ResourceDescriptionNB_Fabric_Cheatsheet.ipynbA runnable reference covering common patterns in Fabric notebooks — Spark/Pandas interop, file I/O, Delta Lake (MERGE / OPTIMIZE / time travel), SQL magic, parameters, notebookutils, performance tips. Every demo cell creates its own sample data, so it runs top to bottom with no setup.NB_Template.ipynbA blank starting point for a standard read → transform → write notebook. Pre-wired with the Variable Library pattern, source/target lakehouse resolution, parameter cell, audit columns, try/except writes, and a validation read. Copy and fill in.

More notebooks and patterns will land here over time.

How to use

Each resource is a single .ipynb file. To use one:


Download the notebook.
In your Fabric workspace: New → Import notebook → Upload.
Attach a lakehouse (any lakehouse works for the cheatsheet; the template expects a Variable Library — see notes inside it).
Run cells in order.


Both notebooks target the Synapse PySpark runtime (the Fabric default). No external libraries required.

Why this exists

Most Fabric documentation answers "how does this one thing work?" — but when you sit down to write a notebook from scratch, you spend half your time remembering the snippet for the thing you've written a dozen times before. These resources are the snippets. Open the cheatsheet, copy what you need, move on.

The template captures the same idea at a larger scale: every Silver / Gold-layer notebook tends to follow the same shape. Starting from a template that already handles parameters, lakehouse resolution, audit columns, and validation means more time on the actual business logic and less on the scaffolding.

Contributing

Pull requests welcome. If you've got a Fabric notebook pattern that other people would find useful, open a PR. Keep the same principles:


Runnable. Self-contained, no external dependencies, sample data inline.
Documented. Every code cell preceded by a markdown cell explaining what it does and why.
De-identified. No client names, internal table names, or environment-specific paths.


License

MIT — use, modify, and redistribute freely.
