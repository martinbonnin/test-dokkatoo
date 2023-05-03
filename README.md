To reproduce:

```
git clone https://github.com/martinbonnin/test-dokkatoo
cd test-dokkatoo
git checkout 3ccb91b
./gradlew dokkatooGeneratePublicationHtml --rerun-tasks
```

Output is:

```
> Task :module-1:dokkatooGeneratePublicationHtml
Generated Dokka HTML publication: file:///Users/mbonnin/git/test-dokkatoo/module-1/build/dokka/html/index.html

> Task :module-2:dokkatooGeneratePublicationHtml
Generated Dokka HTML publication: file:///Users/mbonnin/git/test-dokkatoo/module-2/build/dokka/html/index.html

> Task :dokkatooGeneratePublicationHtml
Generated Dokka HTML publication: file:///Users/mbonnin/git/test-dokkatoo/build/dokka/html/index.html

BUILD SUCCESSFUL in 3s
```

But there is no `index.html` in `build/dokka/html/index.html`

```
$ ls build/dokka/html/index.html
ls: build/dokka/html/index.html: No such file or directory
```