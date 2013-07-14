<!-- #Idea -->

This is the repository for the RubyJams user group in Copenhagen. The purpose of RubyJams is to make it straightforward for anyone to start a ruby user group where they live.

This minimalistic static website is based on:

* [Nanoc](http://nanoc.ws) as a static site generator
* [slim](http://slim-lang.com) as a simplified markup language for layouts
* [sass](http://sass-lang.com) to streamline your stylesheets
* Markdown to write blog posts with a natural syntax
Check out the [Gemfile](https://github.com/fuzzytern/rubyjams/blob/master/Gemfile) for more details on what's being used.

The website features a homepage presenting the Copenhagen RubyJams group and its ambitions, as well as a blog and a link section for relevant resources. To set up something similar in your city, just follow these straightforward steps:

1. Fork RubyJams and tweak the content if needed to match the needs of your group. You might also want to edit the `deploy` task of the Rakefile to match your server setup.
2. Deploy it to some domain (`rake deploy`). You can get *city.rubyjams.org* for free under certain conditions (see note below).
3. Find people and a place. E.g. create a post on the blog saying you're looking for a place and calling for people to join. (To create a new post: `rake new`)
4. Make it happen. E.g. create a post on the blog where you indicate the date and the place of the first jam.
5. Congrats, you're done. Make sure to keep the blog up to date (hopefully you have plenty of people keen to take on that task now). Also check the [Nanoc documentation](http://nanoc.ws/docs/) for further customisation.

Note: It's up to you and your group to decide whether you want to keep any affiliation with RubyJams on your website. If you share the same purpose and vision, we recommend that you keep the *purpose* and *membership* sections of the home page intact, as well as keeping the name RubyJams for the group. This will help us create a coherent international ruby community based on common principles. This will also enable you to register your website under the form of *city.rubyjams.org* for free.

Note 2: The whole concept is at its very early steps. Please feel free to make any suggestions by amending this README file (in a PR) or by contacting me at nicolas@cybercrumbs.net.

<!-- #Raketasks -->
