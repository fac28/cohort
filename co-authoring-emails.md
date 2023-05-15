# Creating co-authored commits

You can find more information in [GitHub Docs](https://docs.github.com/en/github/committing-changes-to-your-project/creating-and-editing-commits/creating-a-commit-with-multiple-authors)

Type your commit message and a short, meaningful description of your changes. After your commit description, instead of a closing quotation, add two empty lines.

```javascript
$ git commit -m "Refactor usability tests.
>
>
```

On the next line of the commit message, type Co-authored-by: name <name@example.com> with specific information for each co-author. After the co-author information, add a closing quotation mark.

If you're adding multiple co-authors, give each co-author their own line and Co-authored-by: commit trailer.

```javascript
$ git commit -m "Refactor usability tests.
>
>
Co-authored-by: name <name@example.com>
Co-authored-by: another-name <another-name@example.com>"
```

## Cohort's emails

| Name | Github email |
| ---- | ------------ |
| Alphonso     |              |
| Cameo     ||
| Elisabeth     |              |
| Mark     |home@markhanley.co.uk|
| Simon     |              |
| Taha     |              |
| Thomas     |tom@team-freeman.com|
| Zakarie     |zakariaali350@gmail.com|
