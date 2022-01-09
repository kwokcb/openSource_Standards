*This is WIP*. (Note, it's not a bad thing to show WIP for open source stuff...)

# Starting "Syntax"

When starting out with a repo of your own or in this case cloning someone else's repo it's always useful to 
look at what I'll coin as the "syntax" or the "conventions" of the repo.

These are all small things but if / when it comes time to contribute something back knowing the "conventions"
helps to get things committed.

Some conventions to watch out for:

## 1. Code

This should be pretty straight-forward for formating for those that have coded before. It's
basic stuff like using of "tabs" vs "spaces" for indents, the indentation style, whether you have
spaces between braces `()` etc. In some cases this will be provided say through something like 
a clang format file which declares the rules for the syntax. Other times, you may just need to read
the code and figure out, or when in doubt just ask. 

Various companies may have their "standard" but be wary that even within the same company there may be more than one 
"standard". A suggestion is to take into account "locality" -- i.e. within the code / library / module of a given format keep
that syntax but if there is mixing in / with other modules / libraries switch as necessary. As there is
no "one standard to rule them all" do what's best.

Some things like names of variables are a bit harder to keep track of, at least in an automated way.
e.g. Check what is being used underscores between workds, camel-case etc. Namig conventions for public
vs private data members, function names, local vs global variables can all have their own rules.

The following is a small contrived C++ example. Here camelcase is being used with uppercase starting for classe names.
Static globals are all in upper case and user undercores, public  members variabels don't use an underscore,
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

2. Documentation

Probably something folks thing less about is what convention should be used for documentation. 

Code documentation can generally be generated using something like doxygen of which there are 
many different format variables possible. What format is being used is less important than
deciding to actually document :). Even if the current repo your contributing to is not documented,
it doesn't hurt to suggest and provide docs for new code. After all, it's something your contributing
for other folks and they need to understand it.

Some tips which may be useful to help is determine if something is a publicing facing interface
or not. If not then determine is it worth to document extensively -- maybe not. Of course minor interfaces 
like an `add` function can require minimal documentation such as "This function adds two vectors together",
where the actually argument documentation can be skipped.

Then comes documentation which is at a higher level -- and generally not generated.
There can be many forms to eventually ship the documentation to. There are a large number of
free converters between formats which are for the most part non-lossy. For documents which
require scientific formulas you can go "old-school" and use Latex for which there are utilities
to convert.

The decision is then what will be your target format. Markdown and markup are some easy to use choices as there are
plug-ins to various editors like Visual Studio Code or Atom which allow for WYSIWYG. 

Some documentation such as design or standards specifications tend to not be in this format
as these generally need to go over review and iteration with various collaborators and certain
utilities are better for this. Some choices include using things like Google Docs and Confluence (wiki)
can be used. 

As for accompanying diagrams and images there are also a number of good free tools there. 
