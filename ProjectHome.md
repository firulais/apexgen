# Summary #

ApexGen is a utility to generate Oracle Application Express (Apex) pages and page components based on a PL/SQL API, in a fraction of the time it takes to manually create report and form pages. ApexGen is released as open source under a BSD license.


# Introduction #
I love <a href='http://apex.oracle.com'>Oracle Application Express</a> and its declarative, metadata-driven approach to application development. But after the initial excitement, I quickly became bored with the tedious process of setting up reports and forms manually. There is typically a lot of clicking around to change the wizard-generated pages and components and the developer has to wait for pages to reload every time changes are saved in the web-based Application Builder.

I am also a big fan of code generators, and when I saw the Apex export files and examined its use of the wwv\_flow\_api package, I realized that it would be possible to generate scripts to set up Apex report and form pages with less work. ApexGen is the result of studying the Apex export files and the Apex dictionary views, and reverse-engineering the wwv\_flow\_api package (not very difficult, given its descriptive procedure and parameter names).

I realize that wwv\_flow\_api, being undocumented and unsupported, is subject to change without notice and that unless one is careful, there is a risk of corrupting your Apex metadata. However, I feel that the benefits outweigh the potential risks.

It would certainly be great if Oracle made available an official, documented and supported API to programmatically manipulate the Apex repository. Please, nice guys at Oracle, could you add that in a future release of Apex?

# Main Features #
  * Generate Apex pages programatically using a PL/SQL API, saving hours of manual work
  * Generate report pages and form pages based on database table metadata
  * Generate report columns with pretty column headers and edit links
  * Generate form items based on column metadata (datepickers for dates, dropdown lists for foreign keys, textareas for large text fields, etc.)
  * Set required/optional label templates based on nullability of column
  * Populate field popup help based on column comments
  * Generate page processes for fetching and updating data via package-based API instead of Automatic Row Processing

# Credits #
ApexGen was designed and written by <a href='http://ora-00001.blogspot.com'>Morten Braten</a>