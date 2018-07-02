# Jekyll Hyperlink Post Titles
Automatically looks for post titles in the content and replaces the first occurrence with a hyperlink.

## Installation  
1.  Place the main `jekyll-hyperlink-post-titles.rb` file into the Jekyll `_plugins` folder  
2.  And add the following to your site's _config.yml  

```yaml
plugins:
  - jekyll-target-blank
```

## Usage  
- Simply install the plugin, re-build your site, and the plugin will start doing the work for you without any configuration.  
- Every post will be processed `post_render`, and will search the text copy content of each post for any matching words or phrases which correspond to toher posts existing on your blog.  Once the first occurance of an existing post's title is found in the body text, that word or phrase will be raplced with an anchor tag pointing to the URL of the post by the same name.

### Example  
Your site has multiple posts by these titles:
- Bicycles  
- Cooking  
- Hobbies  
- Postmodernism is stupid  
- Progrssivism is silly  
- My journal entry for the day

The hobbies post body has this first paragraph:  
> I like to have fun, and I like my hobbies very much.  My favorite hobbies include flying, cooking, mountain biking, and bicycles in general.  Also, did I mention I love cooking and tomatoes?

After the plugin processes that post, it'll be output like this:  
> I like to have fun, and I like my hobbies very much.  My favorite hobbies include flying, [cooking](https://example.com/cooking), mountain biking, and [bicycles](https://example.com/bicycles) in general.  Also, did I mention I love cooking and tomatoes?

Notice that the first occurance of `bicycles` and `cooking` was replaced with an anchor tag.  
Also notice that the second occurance of `cooking` was left alone, and not replaced.


## Credits  
The starting point for this plugin [Keith Mifsud](https://keith-mifsud.me)'s [Jekyll Target Blank](https://github.com/keithmifsud/jekyll-target-blank). Thank you ❤️

## Legal  
This software is distributed under the MIT license.

© 2018 - [Andre Bulatov](https://andrebulatov.com) and approved contributors.
