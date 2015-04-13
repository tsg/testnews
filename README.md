# Testnews

A simple HN / Reddit clone based on [Drum](https://github.com/stephenmcd/drum).

It's purpose is to serve as an example monitored application for [Packetbeat](http://packetbeat.com). The deployment consists of:

 * Nginx
 * Gunicorn
 * PostgreSql
 * Memcached

## Deploy

It's based on fabric. Run against a Debian machine:

    fab all

To load some fresh data from HN and Reddit:

    fab manage:"poll_rss https://news.ycombinator.com/rss http://www.reddit.com/r/programming/.rss"
