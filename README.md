# Releases

See all releases and the status of repos at releases.elementary.io

## Updating Data

`_data/repos.json` is automatically rebuilt from a GitHub Action, but you can build it for local development:

First, make sure you have `pip` and `PyGithub`:

```sh
python -m pip install --upgrade pip
pip install PyGithub
```

Then run `release.py`:

```sh
python release.py
```

## Building

You'll need the following dependencies:

```
ruby-full
build-essential
zlib1g-dev
```

We recommend installing gems to a (hidden) directory in your home folder:

```sh
echo '' >> ~/.bashrc
echo '# Install Ruby Gems to ~/.gems' >> ~/.bashrc
echo 'export GEM_HOME="$HOME/.gems"' >> ~/.bashrc
echo 'export PATH="$HOME/.gems/bin:$PATH"' >> ~/.bashrc
echo '' >> ~/.bashrc
source ~/.bashrc
```

Install jekyll and bundler:

```sh
gem install jekyll bundler
```

Install gems:

```sh
bundle install
```

Build and serve locally with:

```sh
bundle exec jekyll serve --host 0.0.0.0
```

The site should now be available at http://0.0.0.0:4000/ on your local machine, and your local machine's IP address on your network—great for testing on mobile OSes.
