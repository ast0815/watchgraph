  watchgraph
==============

Tool to monitor the output of a command in a periodically refreshed graph in the shell

  example
-----------

`watchgraph 'cat /proc/loadavg | cut -d " " -f 1-3'`

    2.2 ++-B######+---+--+--+---+--+---+--+--+---+--+---+--+--+---+--+---+-++
        +      +  B######B######   +      +      +      +     +  No1 **A*** +
      2 ++                      B######                          No2 ##B###++
        |                              B#####                    No3 $$C$$$ |
    1.8 ++ C$$$$$$C$$$$$$C$$$$$$C$$$$$$      B######B######                ++
        |                              C$$$$$C$$$$$$C$$$$$$B######B######   |
        |                                                                B  |
    1.6 ++                                                                 ++
        |  A******                                                          |
    1.4 ++        A*****                                                   ++
        |               *                                                   |
    1.2 ++               A*****                                            ++
        |                      *                                            |
      1 ++                      A*****                                     ++
        |                             *                                     |
        |                              A*****                               |
    0.8 ++                                   A*****                        ++
        |                                          *                        |
    0.6 ++                                          A******                ++
        +      +      +     +      +      +      +      +  A******A******   +
    0.4 ++-+---+--+---+--+--+---+--+---+--+--+---+--+---+--+--+---+--+---A-++
      36:20  36:30  36:40 36:50  37:00  37:10  37:20  37:30 37:40  37:50  38:00
