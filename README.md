mojox-ioloop-server-starttls
============================

MojoX::IOLoop::Server::StartTLS - adding STARTTLS support to Mojo::IOLoop::Server

Installation:

    perl Makefile.PL
    make install

Usage:

    MojoX::IOLoop::Server::StartTLS::start_tls(
        $server,
        $stream,
        undef, # hash of TLS options
        sub {
            my ($handle) = @_;
            # Callback after TLS upgrade (negotiation not done, new 'accept' event fires when it is)
        }
    )
