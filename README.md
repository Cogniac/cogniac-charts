# Cogniac Charts Repo

This is a repository for hosting public helm charts.  It is hosted using 
GitHub Pages.  To view the landing page, go to [https://cogniac.github.io/cogniac-charts/index.html].

### Adding a chart

```console
$ git checkout -b some_new_chart
$ helm package mychart
$ mv mychart-0.1.0.tgz docs
$ helm repo index docs --url https://cogniac.github.io/cogniac-charts 
$ git add docs/mychart-0.1.0.tgz docs/index.yaml
$ git commit -m 'adding new chart for ...'
$ git push -u origin some_new_chart
```

Create a PR for merging branch `some_new_chart` into master.  When this has been reviewed, approved,
and merged, you can run: `helm repo add mychart https://cogniac.github.io/cogniac-charts`
