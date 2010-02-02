memcached module for PHP
========================

This module requires zlib library, used for on-the-fly data (de)compression.
Also, you'll need memcached to use it =)

This version adds the tags_delete function that was added in memcached-tags (branch of memcached-tag)

The memcached website is here: <http://www.danga.com/memcached/>

You will probably need libevent to install memcached. You can download it here: <http://www.monkey.org/~provos/libevent/>

### Original Maintainers:

* Mikael Johansson <mikael@synd.info>
* Antony Dovgal <tony2001@phpclub.net>

### New Maintainers

* Kevin Morey <kevin@kmorey.net>
* Josh Turmel <jturmel@gmail.com>
* Chris Vaughn <chris@cvaughn.com>

Usage:

For original wiki visit: http://code.google.com/p/memcached-tag/

Using tags_delete()

It accepts one parameter, either a string or array.

Example passing string:

$memcache->tags_delete('tag_1 tag_2'); // This will delete all stores that have both tag_1 and tag_2 attached to their keys.

Example passing array:

$tags = array('tag_1 tag_2', 'tag_3 tag_4');
$memcache->tags_delete($tags); // This will delete all stores that have both tag_1 and tag_2, and then it will delete all stores that have both tag_3 and tag_4.  Simply put, passing in as array treats each item in the array as if you were passing it in as a string as in the first example.

Enjoy!
