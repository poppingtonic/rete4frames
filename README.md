Rete for Frames
====

Clojure RETE implementation for frames

Manners Benchmark Table
----

<table>
<tr><td>Test</td><td>CLIPS v 6.24 (msec)</td><td>rete4frames v 5.0.0 (msec)</td><td>rete4frames v 5.1.0 (msec)</td><td>factor</td></tr>
<tr><td>manners8</td><td>1.4</td><td>85</td><td>67</td><td>x 48</td></tr>
<tr><td>manners16</td><td>18</td><td>208</td><td>222</td><td>x 12</td></tr>
<tr><td>manners32</td><td>266</td><td>1204</td><td>1261</td><td>x 4.7</td></tr>
<tr><td>manners64</td><td>8528</td><td>9374</td><td>9090</td><td>x 1.1</td></tr>
<tr><td>manners128</td><td>311231</td><td>112185</td><td>76407</td><td>x 0.25</td></tr>
</table>

Test results obtained on the same hardware and OS (Linux Mint 16, Petra) 19 august 2014.
As can be seen from the results, rete4frames initially far behind and then starts to catch up CLIPS v 6.24.
On the most difficult test rete4frames four times superior to CLIPS v 6.24.
(I must say CLIPS 6.30 is two orders faster than 6.24)

To get the results run in REPL:

```
(require 'rete.core)
(in-ns 'rete.core)
(app "run:asynch" "examples/manners.clj" "examples/manners_f8.clj")
```
The benchmark table for Waltz algorithm is in [Waltz Benchmark Table] (https://github.com/rururu/rete4frames/blob/master/doc/waltz_benchmark.md)

To include Rete for Frames into your Leiningen project:

```
:dependencies [[rete "5.1.0-SNAPSHOT"]]
```
Running examples:
```
(require 'rete.core)
(in-ns 'rete.core)
(app "run:asynch" "examples/mab.clj") ;; Monkey and bananas..
(app "run:synch" "examples/zebra.clj") ;; Who drinks water, who owns zebra..
(app "run:asynch" "examples/auto.clj") ;; Automotive Expert System..
```
How to include Rete for Frames into your Java programs see example [Eclipse project] (https://github.com/rururu/rete4frames/blob/master/Rete4framesEclipseTest/).

For further information see [Documentation] (https://github.com/rururu/rete4frames/blob/master/doc/intro.md)

Copyright and license
----

Copyright © 2014 Ruslan Sorokin.

Licensed under the EPL (see the file epl.html).
