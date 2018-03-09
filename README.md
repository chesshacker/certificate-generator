# Certificate Generator

Once in awhile, I need a self-signed certificate. Typically, I google how to
generate a self-signed cert, and eventually I stumble my way through the openssl
commands. That works, but I decided to solve this for myself once and for all.

This project runs openssl in Docker to generate private keys and certificates,
given a configuration file from the input directory.

## Dependencies

You need to have [Docker](https://www.docker.com/community-edition) installed.

To run the generate script, you should also have access to a `bash` shell. On a
Mac, you are all set... just open up Terminal. On Windows, you might try using
[Git Bash](https://git-scm.com/downloads).

## Usage

Either change the values in the `input/default` file and run `./generate` or
create your own file in the same directory, and run `./generate your_filename`.

If all goes well, this will generate three files in the `output` directory. A
`.crt` file with your certificate, a `.key` file with your private key and a
`.csr` file with the certificate signing request.

## Development

There isn't much to this tool. All the relevant openssl commands can be found in
`docker/entrypoint`. If you do change the entrypoint, you can rebuild the docker
image with the `docker/build` script.

## Contributions

I am not an expert on certificates. If you have any suggestions on how I could
do this better, please create an issue or send a pull-request. Thank you!
