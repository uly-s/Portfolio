# Portfolio

## https://www.lottery.ok.gov/ - My current masterpiece (scroll for other repos/projects)

  I built roughly 90% of the state lottery website, it utilizes a custom Vue/Webpack build of my making bolted on top of an old .Net Framework codebase and back end. This allowed the full capabilities and usage of Vue components/directives for the dynamic portions of the site and plain HTML/CSS/CSHTML for all static portions. Tinymce is heavily integrated into the site allowing non-dev control of large amounts of content/copy across most pages, I also extended tinyMCE with OLC specific custom menu options allowing non-dev users to insert card style components/content independently of the dev team. The website is backed by a database driven CMS whose users have the ability to create dynamic pages and articles on the site for promotions, press releases, etc etc that can then be edited with TINYMCE. Assets and misc documents on the site are controlled and managed from the agency CDN (Azure) we implemented right before the actual website, it features a web tool/interface mimicking a simple file system and an api implemented via Azure app service allowing agency staff to upload any file they need available online themselves.
  
  I was taught by the senior dev I was working under that our goal for the app/website/cms was to allow others in the agency to take ownership of the features we implemented and perform their duties totally indepdently of us the developers. I built the site around that principle whenever possible and with said Seniors help on the backend everything from new lottery games/scratchers, promotional pages, and carousel/sliders can be set by agency members without writing any code at all.
Performance/Implementation wise the site is configured such that each page (bar some) has it's own entry-point and maybe stylesheet defined in the webpack.config. This ended up synergizing quite well with MVC's _Layout.cshtml templating system as the global dependencies / bundles could be included once in the master layout leaving the script for any individual page quite lean. The entire site is laid out with bootstrap using bootstrap utility classes + extra html absolutely whenever possible instead of custom css (tailwind esque). SCSS was used to write all style code for the site typically with one .scss file per page (With the vue components having their specific style code to themselves in the Vue single file component format), mixins were utilized quite heavily for the site to enforce consistent style and responsive behavior, but at the end all of our custom in house CSS and vendor style sheets are bundled into one global stylesheet by webpack that can be effectively minified/optimized. 

  As the lottery has many users in the boonies of Oklahoma with slow internet great care was taken to prevent any unnecessary bloat from npm packages and assets were optimized whenever possible, the production build made heavy use of treeshaking and code splitting such that the most heavy duty dynamic pages on the site still end up with just under a megabyte of javascript total. The build was in the style of "fat dev dependencies, lean client dependencies", the outputted code was 100% client side and no Node.js server code used in production at all. This had great implications for security as the production servers didn't even need to have Node.js installed despite our extensive use of it in development. 

  Overall it ended up being pretty clean and modular, was quite pleasant to work on and you never had to think twice about the right way to extend the repo with new code. 
  
  ## https://github.com/uly-s/Data-Structures
  
  This was my first repo and truly how I cut my teeth programming and found my passion for it. Features about 35-40 small to medium sized C++ implementations of various data structures and algorithms lovingly organized into my own mini STL.
  
  ## https://github.com/uly-s/Machine-Learning-C
  
  My first machine learning projects, two from scratch neural networks in about 1,000 lines of C++ each, truly excruciating to write and debug but I got it working. Then I learned about python and never, ever looked back.
  
  ## https://github.com/uly-s/Machine-Learning
  
  Quite a few different machine learning projects in the form of various neural network architectures implemented from scratch in numpy, with Keras/Tensorflow, or with a mix of both. These projects brought me to the level where I could implement an algorithm or architecture from the psuedocode/description in a research paper instead of just following some tutorial blog post. For this reason I feel confident asserting I am a step above pytorch/tensorflow script kiddy in the realm of machine learning.
  
  ## https://github.com/uly-s/scrap-heap
  
  Miscellaneous college assignments and code I wrote while tutoring. Highlights include:
  
  - A random CUDA project I did that can take a dataset of images and perform a lossy compression to 1/64th original memory size all in an optimial concurrent work flow.
  - Cute little python GUI I wrote for rolling dice and such for dungeons and dragons
  - "inclearn" some sort of weird optimization algorithm I wrote in a feverish fugue state on a whim.
  - a fair amount of C systems programming projects with posix constructs like monitors, message queues, semaphores, POSIX threads, IO system calls etc.
  - Some SQL schema for a large database project in OU's database course
  - A bison/yacc implementation of a simple algol style programming language for a principles of programming languages class.

## https://github.com/uly-s/2TML && https://github.com/uly-s/foundry-sval

  If you got this far you may have noticed that while I've done a lot of self teaching and projects on my own I have done ~0 open source contribution and collaboration, this is the early stage of my attempt to fix that with a project of my own. 
  The goal of this project is a digital native format and language/applications for tabletop rpgs. Essentially bringing them into the 21st century while preserving and enhancing what makes TTRPGs special and different from videogames, by defining them in a machine readable and computable system instead of natural language documents. 
  Write now it's mostly a maniacal fever dream but everyone I've explained the project too says I'm onto something. I look foward to being able to dedicate regular time to it in the future and bring others on.
  
  

