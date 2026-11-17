# Contributing to BetterAngle

Thanks for helping. A few rules keep releases safe for everyone who has the app installed.

## Releases

- Every push to `main` builds the app with GitHub Actions and publishes a new release, which installed copies
  pick up automatically. Open a pull request and merge only changes that are ready to ship.
- The workflow raises the patch version by itself. To release a specific version, change `VERSION` in the same
  push.
- Releases are never left as drafts.
- Versions must match across `VERSION`, `CMakeLists.txt`, `include/shared/State.h` and `RELEASE_NOTES.md`
  (`scripts/bump_version.ps1` keeps them in step).
- To write the notes for the next release yourself, add its `### BetterAngle Pro vX.Y.Z` heading at the top of
  `RELEASE_NOTES.md`. Otherwise the release gets a generic line.

## Input handling

- Never send synthetic keyboard or mouse input to the game, and never install input hooks or drivers.
- Dive/glide transitions offer two modes, *Block input* and *Blend*. See [docs/INPUT_LOCK.md](docs/INPUT_LOCK.md).

## Local builds

Local builds are for development only. See *Building from source* in the [README](README.md).
