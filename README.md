# sfkendo.github.io

The official website for the San Francisco Kendo Dojo, powered by GitHub Pages and Jekyll. Please visit [www.sfkendo.org][1] for more information on the San Francisco Kendo Dojo.

## Running locally with Jekyll

You will first need to install the Ruby version specified in Gemfile. rbenv is a lightweight Ruby manager that makes installing specific versions of Ruby easier.

```bash
bundle install
bundle exec jekyll serve
```

The site will be available at `http://localhost:4000`. Jekyll will watch for changes and rebuild automatically.

## Updating the enrollment notice

The enrollment announcement shown on the Home, How to Join, and Contact pages is maintained in one place:

```
_includes/enrollment-notice.md
```

Edit the text in that file to update the enrollment message across all three pages at once.

## Updating instructors

**To add or remove an instructor from the page**, edit `_data/instructors.yml`. Each entry looks like:

```yaml
- name: Example Sensei
  image: example-300x300.jpg
```

The order of entries controls the order instructors appear on the page.

**To add a photo**, place the image file in `assets/instructors/` and add a corresponding entry to `_data/instructors.yml`.

**To remove a photo**, delete the image from `assets/instructors/` and remove its entry from `_data/instructors.yml`.

[1]: http://www.sfkendo.org
