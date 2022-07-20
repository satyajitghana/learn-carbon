# learn-carbon

```bash
git clone --recurse-submodules https://github.com/satyajitghana/learn-carbon
```

Install Homebrew

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
echo 'eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"' >> /home/codespace/.profile
eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"
```

Install Dependencies

```bash
brew install bazelisk
brew install llvm

# force to use brew's llvm
export PATH="$(brew --prefix llvm)/bin:${PATH}"
```

Run Explorer

```bash
cd carbon-lang
bazel run //explorer -- ./explorer/testdata/print/format_only.carbon
```
