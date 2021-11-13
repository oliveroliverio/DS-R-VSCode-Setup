# [VSCode R-User Data Science Setup: R, R LSP, RMarkdown All-In-One](https://www.youtube.com/watch?v=PLUOdk0sm5M)

VSCode extensions
- R
- R LSP Client (note: now integrated in VSCode)
- R Markdown All in One (I had to google this to install)

Make new file
`test-R-Markdown.rmd`

```
library(tidyverse)

16+1

df <- mtcars
```

Tried to knit: `cmd shft p`, "knit"
Got error: "Knitting requires the {rmarkdown} package

Install package `rmarkdown`
Go to R console/terminal
```
install.packages("rmarkdown")
```

Tried knitting again
Error: "pandoc version 1.12.3 or higher is required and was not found"

Google error, found out pandoc isn't an R package but a unix app.  See if installed
```
pandoc --version
```
Output: command pandoc not found.
So not installed
Install via brew

```
brew install pandoc
```

Tried knitting again
Error: "no package called tidyverse"
Install tidyverse package
