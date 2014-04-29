# Feed

The feed.py program allows you to send commands to and query the robot.

# Examples

## Querying the robot

./feed.py --verbose --command q

## Calibrate the robot

./feed.py --verbose --command c

## Force calibrate the robot, with string lengths of 100mm each

./feed.py --verbose --command f100,100

## Pen down

./feed.py --verbose --command d1

## Pen up

./feed.py --verbose --command d0

# Setup with crontab

This is what I have in my crontab:

*/10 * * * * cd /home/pi/cursivedata/client/ ; ./feed.py --verbose --server --send-status >> log 2>&1

# Python Requirements

* argparse
* requests
* serial