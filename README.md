# Source Files
Files to source in orgdata via `EXTRA` columns either for files or filegroups tables.

Specify with:
- `SourceR("fileName.R")` for R files
- `SourceStata("fileName.do")` for Stata files

When sourcing an R file, it's advisable to use `kh_load()` function to load R packages. Add these line on top of your R file to make `kh_load()` available.

```R
source("https://raw.githubusercontent.com/helseprofil/misc/main/utils.R")
kh_load(dplyr, ggplot) #examples of packages to load
```

## More columns
If the souce code will need mutate columns other than those in the original data, please define the needed column in `TAB` or `VAL` with value `<NA>` 
