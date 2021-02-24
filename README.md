# dbic-to-red

Generate Red models from a DBIx::Class Schema

# Synopsis

   ./dbic-to-red --schema Foo::Schema --outdir lib6 --class_prefix Foo::DB

# Description

This makes a quick attempt at generating [Red](https://github.com/FCO/Red) model 
classes from a [DBIx::Class](https://github.com/Perl5/DBIx-Class) schema definition.

It doesn't connect to a database, but simply queries the API of the schema to
determine the result class definitions and the relations.  

You might want to use this rather than generate new classes from a database using
other tools if, for instance, your source DB is one which isn't supported by Red
(e.g. Oracle, Sybase,) or you have custom relations in your schema which aren't
represented in the source DB by, say a foreign key constraint.

# Usage

Right now this isn't very polished, so it's basically copy the dbic-to-red and
the `red_model.tt` to the directory in which your schema library is and
run the script with the required arguments, then you can copy your new
directory away to wherever you want it.

# Requirements

You will of course need DBIx::Class installed, additionally you will need:

    * Template
    * Path::Class
    * Getopt::Long
    * Module::Load

# Licence

It's a kind of [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/) thing.


