# Pre-8-Cleanup
Code cleanup before migrating to Drupal 8

Filter formats had numeric keys in Drupal 6 but were changed to machine names in Drupal 7. However the
core upgrade process didn't change sites that were previously D6 to machine names. The migrate path from
D7 to D8 is currently choking on the numeric filter formats. It seems easiest to just clean them up
before attempting to migrate.

This is not guaranteed to work on every site. There may be other custom or contrib tables using the old format values.
