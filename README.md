GitHub Changelog Generator
==================

[![Gem Version](https://badge.fury.io/rb/github_changelog_generator.svg)](http://badge.fury.io/rb/github_changelog_generator)

Changelog generation has never been so easy.

This script automatically generate change-log from your tags and merged pull-requests.

## Installation:
	[sudo] gem install github_changelog_generator

## Usage

	github_changelog_generator -u github-username -p github-project

In output you will get `CHANGELOG.md` file with *pretty Markdown-formatted* changelogs in your current directory.

### Params:
See `github_changelog_generator --help` for detailed usage.

    Usage: changelog_generator --user username --project project_name [options]
        -u, --user [USER]                Username of the owner of target GitHub repo (required)
        -p, --project [PROJECT]          Name of project on GitHub (required)
        -t, --token [TOKEN]              To make more than 50 requests this script required your OAuth token for GitHub. You can generate it on https://github.com/settings/applications
        -h, --help                       Displays Help
        -v, --[no-]verbose               Run verbosely
            --[no-]issues                Include closed issues to changelog. Default is true
            --[no-]pull-requests         Include pull-requests to changelog. Default is true
        -l, --last-changes               Generate log between last 2 tags only
        -f, --date-format [FORMAT]       Date format. Default is %d/%m/%y
        -o, --output [NAME]              Output file. Default is CHANGELOG.md
            --labels  x,y,z              List of labels. Issues with that labels will be included to changelog. Default is 'bug,enhancement'a

## Examples:
Look at changelog in this project!

### This changelog: [ActionSheetPicker-3.0/CHANGELOG.md](https://github.com/skywinder/ActionSheetPicker-3.0/blob/master/CHANGELOG.md)

Was generated by command:

	github_changelog_generator -u skywinder -p ActionSheetPicker-3.0


## FAQ:
Since GitHub allow to make only 50 requests without authentication it's recommended to run this scrip with key `-t [your-16-digit-token]` that you can easily **[generate it here](https://github.com/settings/applications)**.

So, if you got error like this:
>! /Library/Ruby/Gems/2.0.0/gems/github_api-0.12.2/lib/github_api/response/raise_error.rb:14:in `on_complete': GET https://api.github.com/repos/skywinder/ActionSheetPicker-3.0/git/commits/89678f7d7f66873c858e6cb07bf697192aca6768: 403 API rate limit exceeded for 195.88.177.9. (But here's the good news: Authenticated requests get a higher rate limit. Check out the documentation for more details.) (Github::Error::Forbidden) 

It's time to generate this token or wait for 1 hour before GitHub reset counter for your IP.

## License

Github the Generator is released under the [MIT License](http://www.opensource.org/licenses/MIT).

## Contributing

1. Create an issue to discuss about your idea
2. [Fork it] (https://github.com/skywinder/Github-Changelog-Generator/fork)
3. Create your feature branch (`git checkout -b my-new-feature`)
4. Commit your changes (`git commit -am 'Add some feature'`)
5. Push to the branch (`git push origin my-new-feature`)
6. Create a new Pull Request

**Bug reports, feature requests, patches, well-wishes, and rap demo tapes are always welcome!**

*Improvements more than welcome - they are kindly requested! :)*