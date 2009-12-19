Cabal tips
==========

[Here is basic cabal template](template.cabal).

* `version`: Be mindful of the
  [Haskell Package Versioning Policy](http://www.haskell.org/haskellwiki/Package_versioning_policy)

* `homepage`: Don't use a darcs repository as a homepage.

* `hs-source-dirs`: Consider putting your code in a `src` directory.

* `build-depends`: Specify bounds on the versions of your dependencies. My
  understanding of the PVP is that if you see that you depend on version
  `A.B.C.D` of `XYZ`, you should specify a dependency of `XYZ == A.B.*`.

* `ghc-options`: Use `-Wall` and `-fwarn-tabs`.

* `source-repository`: Specify a source repository. This tells users how to
  download the latest revision and, perhaps more importantly, your preference
  about how they should submit patches.

* Use `cabal check`.

* Verify that your Haddock documentation looks correct. I alias
  `hadd='cabal haddock && firefox dist/doc/html/*/index.html'`.
