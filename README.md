# AMNH Science Visualization Group

An [internal website](https://amnh-sciviz.github.io/) for documenting the projects and prototypes of the Science Visualization Group (SVG) at the American Museum of Natural History.

## Instructions for making changes to the website

### Get a Github account

First, you will need a [Github account](https://github.com/). Once you sign up, ask [an admin](https://github.com/orgs/amnh-sciviz/people) to be added to the SVG Github organization.

### Website structure

The website structure is very "flat." There is the homepage and then a single page for each of our projects.  A project page consists of any amount of text and multimedia (images, audio, video.) The homepage automatically lists all the project pages ordered in reverse chronological order.

All the project pages are contained in the [_projects](https://github.com/amnh-sciviz/amnh-sciviz.github.io/tree/master/_projects) folder.

### Making text edits to pages

For simple edits, you can do this directly on the Github website if you are logged into your account.

On the main [github page](https://github.com/amnh-sciviz/amnh-sciviz.github.io), click on `_projects`:

![Screenshot showing to click on projects](https://raw.githubusercontent.com/amnh-sciviz/amnh-sciviz.github.io/master/assets/img/docs/edit_page_step01.png)

Then click on the page that you want to edit.

![Screenshot showing to click on a project](https://raw.githubusercontent.com/amnh-sciviz/amnh-sciviz.github.io/master/assets/img/docs/edit_page_step02.png)

On this page, click the edit icon on the top right.

![Screenshot showing to click on edit button](https://raw.githubusercontent.com/amnh-sciviz/amnh-sciviz.github.io/master/assets/img/docs/edit_page_step03.png)

Here you will see the "source" of the page like this:

![Screenshot showing source of page](https://raw.githubusercontent.com/amnh-sciviz/amnh-sciviz.github.io/master/assets/img/docs/edit_page_step04.png)

There's an important section at the top of the page that is in this format:

```
---
layout: page
title: AR Shark
image: /assets/img/ar_shark_thumbnail.jpg
year: 2017
permalink: /ar-shark/
---
```

All pages must have these here, so don't delete them! The `title:` and `image:` values are used to populate the homepage. The `year:` is used for ordering the projects on the homepage, which is reverse chronological order. You can further sort within years by adding a month, like `2018-04`.

The `permalink:` determines what the URL for this page looks like. For the example above, the URL would be `https://amnh-sciviz.github.io/ar-shark/`.  Note that the `/` at the end is necessary and would not work without it. If this line was omitted, the default URL would be `https://amnh-sciviz.github.io/projects/ar_shark.html` (not as pretty.)

When in doubt, don't edit anything in the section before the 2nd `---`.  The rest of the page is in a format called "Markdown" which is a simplified syntax for writing HTML. You can view a [Markdown guide here](https://guides.github.com/features/mastering-markdown/) and a [cheatsheet here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

In most cases we will be dealing with just headings, paragraphs, and embedded media. A structure might look something like this

```
## Cool project name

Some text introducing this project

### Technology used

- Microsoft's Hololens
- Google's Tango
- Unity

### Documentation

Here's an embedded image:

![Text describing this image](/assets/img/cool_image.png)

Here's an embedded video:

<video src="/assets/video/arshark.mp4" muted autoplay loop controls></video>

Here's an embedded Youtube video

<iframe width="560" height="315" src="https://www.youtube.com/embed/pOxG4aSQOO8" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

Markdown also accepts arbitrary HTML, so you can add tags that are not supported by Markdown, like videos and iframes.

Once you are finished with your edits, you can click "Preview changes", then scroll to the bottom, optionally add a comment about your change, then click `Commit changes`.  Your changes should be visible in the website in a few moments.

### Embedding multimedia on a project page

Four main types of media tags are supported on this website: images, videos, audio, and iframes (media embedded from other websites such as Youtube or Vimeo)

#### Preparing your media

Before you upload your media, you may need to resize/re-encode them so they don't make this repository too big.

Images on the homepage are **640 x 360**

Videos should be compressed as much as possible (ideally under 10mb.)  If you are using [Handbrake](https://handbrake.fr/), try using the `Web -> Gmail Medium 480p30` setting or `720p` if `480p` is too low resolution. If you require higher resolution, consider uploading to Youtube or Vimeo, and embedding that video player instead.

#### Uploading your media

Once your files are ready, go to the [assets](https://github.com/amnh-sciviz/amnh-sciviz.github.io/tree/master/assets) folder, then click `img` or `video`.

On the top right, you should see a `Upload files` button. Click that, then you can drag-and-drop or choose your files to upload.

![Screenshot showing upload files button](https://raw.githubusercontent.com/amnh-sciviz/amnh-sciviz.github.io/master/assets/img/docs/upload_files.png)

After you uploaded your images, you can link to the like this:

```
Here's an embedded image:

![Text describing this image](/assets/img/cool_image.png)
```

The `Text describing this image` is the image's _alt text_ which is used for screen readers.  You can embed a video like this:

```
Here's an embedded video:

<video src="/assets/video/arshark.mp4" muted autoplay loop controls></video>
```

Note that there are options `muted`, `autoplay`, `loop`, and `controls`. If you `autoplay` the video, it must also be `muted` (browsers don't allow autoplay of sounds).  It's generally a good idea to include `controls`, giving the user the option to play/pause/unmute/etc.

### Creating new project pages

On the main [github page](https://github.com/amnh-sciviz/amnh-sciviz.github.io), click on `_projects`:

![Screenshot showing to click on projects](https://raw.githubusercontent.com/amnh-sciviz/amnh-sciviz.github.io/master/assets/img/docs/edit_page_step01.png)

On this page, click the `Create new file` button on the top right.

![Screenshot showing to click on Create new file button](https://raw.githubusercontent.com/amnh-sciviz/amnh-sciviz.github.io/master/assets/img/docs/create_new_step01.png)

Enter a filename for your new project, e.g. `project_name.md`:

![Screenshot showing to enter a file name](https://raw.githubusercontent.com/amnh-sciviz/amnh-sciviz.github.io/master/assets/img/docs/create_new_step02.png)

Copy and paste the following into the editor, and replace `project name` with your new project's name:

```
---
layout: page
title: Project Name
image: /assets/img/project_name_thumbnail.jpg
year: 2019
permalink: /project-name/
---

## Project Name

Project description here.
```

Note that you must create and upload a new representative project image as described in the [previous section](#Preparing-your-media).

And a reminder that the year determines the order that it will show up on the homepage.

Once you've added the content that you wanted to, you can click "Preview changes", then scroll to the bottom, optionally add a comment about your change, then click `Commit changes`.  Your changes should be visible in the website in a few moments.

**Important!** Any new project page created will automatically added to the homepage.

### Making changes locally

This section is for "power users" and/or if you need to make substantial changes that require you to making a number of changes across the website at once.

First you must have Ruby and bundler installed. For Macs, [RVM](https://rvm.io/rvm/install) for Ruby is recommended.

You can then clone the repository and install/launch Jekyll:

```
git clone https://github.com/amnh-sciviz/amnh-sciviz.github.io.git
cd amnh-sciviz.github.io
bundle install
bundle exec jekyll serve
```

By default, this will launch the website at `localhost:4000`.  Any changes you make should be immediately reflected.  You can manually view the static file output by looking in the `_site` folder.

Any changes to `_config.yml` requires you to restart Jekyll
