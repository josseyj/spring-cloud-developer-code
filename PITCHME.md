# Agenda

* <s>Distributed</s> Micro services
* Fault Tolerance
* Abstraction Overhead
* Code Optionally
* Construction Injection.
* OSS Language Alignment
* Handy tools
  
---

## <s>Distributed</s> Micro services

* Micro service architecture is a spectrum
* Can be applied with in a Monolyth
* Martin Fowler: [Monolyth First](https://martinfowler.com/bliki/MonolithFirst.html)
  > * ... successful microservice stories have started with a monolith ...
  > * ... a system that was built as a microservice system from scratch, it has ended up in serious trouble.
* [Application continuum](http://www.appcontinuum.io/)
  > * ... start anywhere on the continuum depending on how much you know ...
  * [Presentation](http://deck.appcontinuum.io/assets/player/KeynoteDHTMLPlayer.html)
  * Our batch jobs could be different independent modules

---

## Fault Tolerance

* Murphy's law ~ if it can break, it will break
* Netflix Hystrix
  * Circuit Breaker
  * Isolation
    * walk away time outs

---

## Abstraction Overhead

* Avoid unnecessary interfaces
* Interface and implementation together

---

## Code Optionally

* NPE is still a reality
* Don't combine both (within a single unit)

---

## Constructor Injection.

* Spring supports it.
* But the beans look less springy
* Usually strategies are also immutable references
* Works with Mockito (mostly)

---

## OSS Language Alignment

* Non functional tests

---

## Handy tools

* [httpie](https://github.com/jakubroztocil/httpie)
  * http PUT api.example.com/person/1 \
    name=John \
    age:=29 married:=false hobbies:='["http", "pies"]' \  # Raw JSON
    description=@about-john.txt \   # Embed text file
    bookmarks:=@bookmarks.json      # Embed JSON file
* [async-profiler](https://github.com/jvm-profiling-tools/async-profiler)
  * Provides a flame graph
    * ![image](https://github.com/jvm-profiling-tools/async-profiler/blob/master/demo/SwingSet2.svg)
