# PMD Source Code Analyzer Action

This action allows to use PMD Source Code Analyzer from GitHub Actions

## Example usage

```yaml
name: PMD Source Code Analyzer on Push

on: [push]

jobs:
  pmd:
  
    runs-on: ubuntu-latest
    
    steps:
      - uses: hectorgb/pmd-action@v1
      - name: run-pmd
        run: pmd -d ./force-app/main/default/classes -R category/apex/design.xml -f text
