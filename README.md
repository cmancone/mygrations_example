# mygrations_example

This example shows how to use the [mygrations](https://github.com/cmancone/mygrations) tool.

# Usage

 1. Install [mygrations](https://github.com/cmancone/mygrations)
 2. Clone this repository
 3. Put your database credentials in the .env file
 4. From within this repository run `mygrate.py plan` or `mygrate.py apply`.
 5. See the results in the database!
 6. Update the `CREATE TABLE` commands in the `database/*.sql` files, add more files, delete files, etc...
 7. Run `mygrate.py plan` or `mygrate.py apply` to see mygrations do its thing more!

 # General Notes

Remember, the `mygrate.conf` file has mygrations-specific configuration.  It assumes that your actual credentials live in a `.env` file.  I've chosen this because I find it to be common, but if you don't have something like a `.env` file in your system then the current iteration of mygrations may not work for you.  If the file is simply named something else though, that's no big deal: use the `--env` flag when calling mygrations:

```
mygrate.py --env env_file_name plan
```

Also remember that by default mygrations expects the `.env` file and the `mygrate.conf` file to be in the same directory.  Once you have this working properly, you should be able to just copy the `mygrate.conf` file and the `database` directory into your own application repository and then `mygrate.py` there.
