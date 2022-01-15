
**Version 1**: January 15, 2022 

# Starting "Syntax"

When starting out with a repo of your own or in this case cloning someone else's repo it's always useful to 
look at what I'll coin as the "syntax" or the "conventions" of the repo.

These are all small things but if / when it comes time to contribute something back knowing the "conventions"
helps to get things committed.

Some conventions to watch out for:

## 1. Code

This should be pretty straight-forward for formating for those that have coded before. It's basic stuff like using of "tabs" vs "spaces" for indents, the indentation style, whether you have spaces between braces `()` etc. 

In some cases this will be provided say through something like 
a [clang format](https://www.kernel.org/doc/html/latest/process/clang-format.html) file which declares the rules for the syntax. Other times, you may just need to read the code and figure out, or when in doubt *just ask*. 

Various companies may have their "standard" but be wary that even within the same company there may be more than one  "standard". 
A suggestion is to take into account "*locality*" -- i.e. within the code / library / module of a given format keep that syntax but if there is mixing in / with other modules / libraries switch as necessary. As there is
no "one standard to rule them all" do what's best.

Some things like names of variables are a bit harder to keep track of, at least in an automated way. e.g. Check what is being used underscores between workds, camel-case etc. Namig conventions for public versus private data members, function names, local vs global variables can all have their own rules.

The following is a small contrived C++ example. Here camel-case is being used with uppercase starting for classe names. Static globals are all in upper case and user undercores, public  members variabels don't use an underscore,
with private ones do.
```
class MyClass 
{
  public:
     static bool GLOBAL_CONSTANT;
     bool publicVariable
  private:
     bool _privateVariable
}
```

## 2. Documentation

Probably something folks think less about is what convention should be used for documentation. 

### 2.1 Code

Code documentation can generally be generated using something like [doxygen](https://www.doxygen.nl/index.htm) of which there are 
many different format options possible. What  options to use is secondary to
deciding to actually document :). 
Even if the current repo your contributing to is not documented,
it doesn't hurt to suggest and provide docs for new code. After all, it's something your contributing for other folks and they (and you) need to understand it.

One tip which may be useful is to determine if something is a **public** facing interface or not. If not then determine is it worth to document extensively -- maybe not. Of course minor interfaces 
like an `add` function can require minimal documentation such as "This function adds two vectors together", where the actually argument documentation can be skipped.

If your proposing an interface and it requires a lot of documentation this may also be a hint that it's too complicated. It's all good and fine to have
something that may compute something complicated but to have an overloaded
interface could be an indication of a poor design breakdown. Also having too many interfaces may overcomplicate things. 

And lastly if there is a convention used for what interfaces to expose and where, it should be followed. One trivial example is do all data members have "get" and "set" interfaces -- if so follow the precedence. 

### 2.2 Design / Specifications

Then comes documentation which is more involved and aimed to describe higher level information such as designs, specifications, technical articles etc -- and generally not generated. 

There can be many forms to eventually deploy the documentation to. There are a large number of free converters between formats which are for the most part non-lossy. One which handles a fairly large number of formats is `pandoc` For documents which require scientific formulas you can go "old-school" and use Latex for which there are utilities to convert.

The decision is then what will be your target format. [Markdown](https://www.markdownguide.org/) and [markdeep](https://casual-effects.com/markdeep/) are two possible common choices which play nicely with repositories and browsers.
Depending on how generally they are used, inherent support / plug-ins can be found various editors like `Visual Studio Code` or `Atom` which allow for WYSIWYG editing.

For *collaboration* (e.g. live review, iteration) with one or more collaborators something like markdown may be the "final" target but for the source representation other formats may be used depending on the portal.
Some natural choices currently used in standards groups discussions (e.g.  Khronos and ASWF) include things like  [Google Docs](https://docs.google.com/) and [Confluence (wiki pages)](https://www.atlassian.com/software/confluence)
Naturally these can be exported / translated when saved to
your repository or published.

Naturally you will need to decide what is most accessible for your own projects and cost does come into consideration as functionality tiers can be keyed to a cost. 

### 2.3 Making it visual

As for accompanying diagrams and images there are also a number of good free tools there. This will naturally not be extensive and will just mentioned that "diagrams are worth a thousand words" (like images :)). And a good reusable vector diagram can be great for clarity -- especially when adding in how what your contributing fits into a larger ecosystem.

Historically there have been things like [Visio](https://www.microsoft.com/en-ca/microsoft-365/visio/flowchart-software/), but in recent years much of this is available via free online or desktop / app utilities. I've personally used [draw.io](https://drawio-app.com/) for many years since it's simple and has some integrations in editors and portals like confluence and JIRA (*). For non-design there are a plethora of options for things like mind-maps etc.  

Again a lot of it has to do with scale and cost -- wherein the emphasis here is what is "free" or very low cost. 

(*) Project planning / scheduling will be a separate blog topic...
