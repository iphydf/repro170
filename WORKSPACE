# Haskell
# =========================================================

RULES_HASKELL_COMMIT = "af2270b0443cd7befc374b793e281abc10476f27"

http_archive(
    name = "io_tweag_rules_haskell",
    sha256 = "8c866ce2367f1c2d7dfd194a7b4ed4b91540aa70b2f447c086ee0d5f023b00b6",
    strip_prefix = "rules_haskell-%s" % RULES_HASKELL_COMMIT,
    urls = ["https://github.com/tweag/rules_haskell/archive/%s.tar.gz" % RULES_HASKELL_COMMIT],
)

load("@io_tweag_rules_haskell//haskell:repositories.bzl", "haskell_repositories")

haskell_repositories()

load("@io_tweag_rules_haskell//haskell:ghc_bindist.bzl", "ghc_bindist")

# This repository rule creates @ghc repository.
ghc_bindist(
  name    = "ghc",
  version = "8.2.2",
)

register_toolchains("//:ghc")
