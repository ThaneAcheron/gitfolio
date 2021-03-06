<img src="https://i.imgur.com/eA6clZr.png">

# Gitfolio  [![Tweet](https://img.shields.io/twitter/url/http/shields.io.svg?style=social)](https://twitter.com/intent/tweet?text=personal%20website%20and%20a%20blog%20for%20every%20github%20user%20&url=https://github.com/imfunniee/gitfolio) ![GitHub release](https://img.shields.io/github/release/imfunniee/gitfolio.svg) ![GitHub top language](https://img.shields.io/github/languages/top/imfunniee/gitfolio.svg) ![GitHub last commit](https://img.shields.io/github/last-commit/imfunniee/gitfolio.svg) ![GitHub](https://img.shields.io/github/license/imfunniee/gitfolio.svg)
  
### personal website + blog  for every github user

Gitfolio will help you get started with a portfolio website where you could showcase your work + a blog that will help you spread your ideas into real world.

Check out this [live demo](https://imfunniee.github.io/gitfolio/) to see gitfolio in action.


# Getting Started

### Let's Build

a. Clone this repo or simply download it.
```sh
git clone https://github.com/imfunniee/gitfolio.git
```

b. `cd` into the repo you just cloned or downloaded.
```sh
cd gitfolio # Navigate into the project folder
npm i # Install the required dependencies
```

c. Gitfolio is now ready to be used. The command

```sh
node build --name [username]
```
Will build your website using your GitHub username and put it in the `dist/` folder.

d. To run your website navigate to `./dist/index.html` in your browser. [you won't see blogs until you are on localhost]

🎉 Congrats, you just made yourself a personal website!

> if you get stuck somewhere or get an error, please create an issue

### Let's Customize

#### Forks

To include forks on your personal website just provide `-f` or `--fork` argument while building

```
$ node build --name username -f
```

#### Sorting Repos

To sort repos provide `--sort [sortBy]` argument while building. Where `[sort]` can be `created`, `updated`, `pushed`,`full_name`. Default: `created`

```
$ node build --name username --sort created
```

#### Ordering Repos

To order the sorted repos provide `--order [orderBy]` argument while building. Where `[orderBy]` can be `asc` or `desc`. Default: `asc`

```
$ node build --name username --sort created  --order desc
```

#### Customize Themes

Themes are specified using the `--theme [theme-name]` flag when running the `build` command. The available themes are

* `light`
* `dark`
> TODO: Add more themes

For example, the following command will build the website with the dark theme
```
$ node build --name username --theme dark
```

#### Customize background image

To customize the background image just provide `--background [url]` argument while building

```
$ node build --name username --background https://images.unsplash.com/photo-1557277770-baf0ca74f908?w=1634
```

You could also add in your custom CSS inside `index.css` to give it a more personal feel.


### Let's Publish

Head over to GitHub and create a new repository named `username.github.io`, where username is your username. Push the files inside`/dist` folder to repo you just created.

Go To `username.github.io` your site should be up!!


### Updating

To update your info, simply run

```
$ node update
```
This will update your info and your repository info.

To Update background or theme you need to run `build` command again.


### Add a Blog

To add your first blog run this command, make sure the title don't have spaces instead use "-".

```
$ node blog --title my-first-blog
```

This will create a `my-first-blog` folder inside `blog`. Inside `my-first-blog` you will find an `index.html` file which contains all the necessary elements for writing a blog. Customize the content of the file to write your first blog.

This also adds content to `blog.json` file. This file helps in showcasing your blogs on your personal website as [cards](https://imfunniee.github.io/gitfolio/#blog_section). You could customize the JSON object that corresponds your current blog.

Blog Demo? [here](https://imfunniee.github.io/gitfolio/blog/my-first-blog/)

Default JSON Format
```
{
  "url_title": "my-first-blog", // the title you provide while creating a new blog, this appears in url
  "title": "Lorem ipsum dolor sit amet", // main title of blog
  "sub_title": "Lorem ipsum dolor sit amet, consectetur adipiscing elit.", // sub-title of blog
  "top_image": "https://images.unsplash.com/photo-1553748024-d1b27fb3f960?w=1450", // main image of blog
  "visible": true // don't worry about this
}
```

More Arguments for Blog

```
--subtitle [subtitle] : gives blog a subtitle (Deafult : 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.')
--pagetitle [pagetitle] : gives blog page a title
--folder [folder] : give folder a title
```

> (use "-" instead of spaces)


## License
![GitHub](https://img.shields.io/github/license/imfunniee/gitfolio.svg)
