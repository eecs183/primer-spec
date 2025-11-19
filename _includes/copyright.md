## Copyright and Academic Integrity

{% comment %}
  1. Set the copyright_holder variable.
     - IF 'page.authors' (a YAML list) exists, join it into a sentence.
     - ELSE, fall back to 'site.author' (from _config.yml).
{% endcomment %}
{% if page.authors %}
  {% assign copyright_holder = page.authors | array_to_sentence_string %}
{% else %}
  {% assign copyright_holder = site.author %}
{% endif %}

© {{ site.time | date: '%Y' }} {{ copyright_holder }}.

{% comment %}
  2. Check for 'page.ta_authors' (a YAML list).
     - IF it exists, join it into a sentence and print the line.
{% endcomment %}
{% if page.ta_authors %}
  {% assign ta_list = page.ta_authors | array_to_sentence_string %}
*Materials for this assignment were developed with assistance from course staff, including {{ ta_list }}.*
{% endif %}

This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>.

<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">
  <img alt="Creative Commons License" style="border-width:0; display: inline !important; margin: 0 !important;" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" />
</a>

**All materials provided for this course, including but not limited to labs, projects, notes, and starter code, are the copyrighted intellectual property of the author(s) listed in the copyright notice above.** While these materials are licensed for public non-commercial use, this license does not grant you permission to post or republish your **solutions** to these assignments.

It is strictly prohibited to post, share, or otherwise distribute solution code (in part or in full) in any manner or on any platform, public or private, where it may be accessed by anyone other than the course staff. This includes, but is not limited to:

- Public-facing websites (like a personal blog or public GitHub repo).
- Solution-sharing websites (like Chegg or Course Hero).
- Private collections, archives, or repositories (such as student group "test banks," club wikis, or shared Google Drives).
- Group messaging platforms (like Discord or Slack).

To do so is a violation of the university's academic integrity policy and will be treated as such.

Asking questions by posting small code snippets to our private course discussion forum is *not* a violation of this policy.
