# Research Tracker

A single-file, browser-based tracker for research projects — pipeline stages,
software used, milestones, and a literature log. No install, no server, no
account. Everything runs locally and your data never leaves your machine.

Built at the [Microbial Ecology & Environmental Genomics Lab](https://meeg-lab.github.io),
United Arab Emirates University.

**[Open the tracker →](https://meeg-lab.github.io/research-tracker/)**

---

## What it does

**Projects as pipelines.** Each project is a lane of ordered stages you click
through: not started → running → complete → blocked. Running stages show elapsed
time, so a job that has been going for three days — or quietly died four days ago
— is visible at a glance.

**Workflow templates.** Metagenomics, Amplicon, Field work, Institutional study,
Wet lab, Paper, Method dev, and Simple come built in. Stages are editable per
project, can be dragged into any order, and you can save your own workflows or
build them from scratch.

**Software on record.** Every stage carries the tool used. A Software tab rolls
these up across all projects and copies out as a per-project list — most of a
methods section, assembled as you work.

**Literature log.** Paper title, authors, journal, year, lab, the point of the
paper, methods, model organism, and a TL;DR. Look up a DOI or title against
CrossRef to fill the bibliographic fields, paste rows straight from a
spreadsheet, or type them in. Searchable across every field; exports back to TSV.

**Sharing.** A Now view pools everything in flight across all projects. Reports
generate a typeset page you can save as PDF for a supervisor. Share snapshot
produces a standalone read-only HTML file with the data baked in — no storage,
no server, just a file you can email.

## Using it

Download `index.html`, put it somewhere permanent, and open it in a browser.
That's the whole installation.

On macOS, open it in Safari and choose File → Add to Dock to give it its own
icon and window.

## Where your data lives

In your browser's local storage, keyed to the file's location. Nothing is
uploaded and there is no server component. Two consequences worth knowing:

- **Moving or renaming the file** makes the app look empty — the data is still
  in the browser under the old key, but the app won't find it.
- **Clearing browsing data** removes it.

Use **Export** to save a JSON backup, and **Import** to restore. Snapshots are a
second, self-contained form of backup.

The one feature that reaches the network is the CrossRef DOI lookup, which is
opt-in per use. Some browsers block outbound requests from pages opened directly
as `file://`; serving the file over http (including GitHub Pages) removes that
restriction.

## Development

There is no build step and no dependencies. `index.html` is the entire
application — HTML, CSS, and JavaScript in one file. Edit it in any text editor
and reload the browser.

Credit, lab links, and the disclaimer are set in the `CREDIT`, `LEARN`, and
`DISCLAIMER` constants near the top of the `<script>` block.

## Related tools from the lab

- [AmpliLearn](https://meeg-lab.github.io/amplilearn/) — browser-based amplicon
  (16S & ITS) workbench: rarefaction, alpha and beta diversity, ordinations,
  taxonomic composition.
- [MetaLearn](https://meeg-lab.github.io/metalearn/) — browser-based
  metagenomics workbench: QC, assembly, binning, MAG quality, and taxonomy.

## How this was built

Built with AI assistance (Anthropic's Claude), from specifications and review by
the authors. The workflow templates and field definitions come from our own
research practice. We're responsible for the code and how it behaves — if
something's wrong with it, it's ours to fix.

## Known limitations

- Data lives in one browser on one machine. There's no sync and no accounts.
- Moving or renaming the file makes the app look empty (see above).
- The DOI lookup needs an internet connection and may be blocked when the file
  is opened directly from disk rather than served over http.
- No undo. Deleting a project or paper is immediate.

## Feedback

Found a bug or want a workflow template added? Open an issue on this repository.
This is a side tool maintained around research work, so fixes come when they
come — but bug reports are welcome and the file is simple enough that anyone can
edit it themselves.

## Citing

If this tool is useful in your work, please cite it. See `CITATION.cff`, or use
the "Cite this repository" button on the GitHub sidebar.

## License

MIT — free to use, modify, and distribute, provided the copyright notice and
permission notice are retained. See [LICENSE](LICENSE).
