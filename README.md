d3-externs
==========

Full (maybe almost full) ClojureScript extern file for
[Mike Bostock][1]'s great [D3][2] library. It allows to use D3 library
under the Google Closure's advanced optimization. Let me know if I
forget some functions.

## Usage

Download `d3_externs_min.js` and place it in your [Leiningen][4] project
folder, say `./externs/d3_externs_min.js`, then set the externs in the
compiler options of your project as shown below

```clj
	:your-build-name {:source-paths ["src/cljs"]
		              :compiler {:output-to "resources/public/js/modern.js"
                                 :optimizations :advanced
								 :externs ["externs/d3_externs_min.js"]}}
```

### Compatibility

All `lein-cljsbuild` versions supporting `:externs` options. 

> [dotnetwise.com/Code/Externs][3] makes all a bit easier.

[1]: http://bost.ocks.org/mike/
[2]: http://www.d3js.org
[3]: http://www.dotnetwise.com/Code/Externs/
[4]: https://github.com/technomancy/leiningen.git
