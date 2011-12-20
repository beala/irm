#Description#
This is a replacement (really, a wrapper) for the rm command. It uses a trashcan, rather than obliterating the file.
It can be installed in your `.bashrc` file, which then gives you access to it on the command line.

#Usage#
To delete a file:

    irm file_to_delete

It also works with wild cards:

    irm *.jpg

To empty the trashcan:

    irm -e

#Installation#
You can simply append it to your `.bashrc` file:

    cat irm.sh >> ~/.bashrc

Or you can add it to another file:

    cat irm.sh >> ~/.bash_functions

And then import it into your `.bashrc` file by appending:

    if [ -f ~/.bash_functions ]; then
        . ~/.bash_functions
    fi

You can configure which directory is the trashcan by setting the `$TRASH` variable
in the script.
