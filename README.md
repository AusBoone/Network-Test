# Internet-Test

This is a Python script that can be used to ping a remote host to test network connectivity. It uses the ping3 library to send ICMP echo requests to the specified host and measure the round-trip time.

# Usage
To use the ping script, you must have Python installed on your system. You can download the latest version of Python from the official website: https://www.python.org/downloads/

Once you have Python installed, you can download the ping.py file from this repository and save it to your local machine. You can then open a terminal window, navigate to the directory where the script is located, and run the script using the following command:

python ping.py <host> [options]

Replace <host> with the hostname or IP address of the remote host you want to ping. The following options are available:

-c <count> or --count <count>: The number of packets to send. Default is 4.
-t <timeout> or --timeout <timeout>: The maximum time to wait for a response, in seconds. Default is 2 seconds.
-v or --verbose: Print verbose output, including the minimum, maximum, and average round-trip times.
-i <interval> or --interval <interval>: The interval between pings when running continuously, in seconds. Default is 1 second.

# How it works
The ping script uses the ping3 library to send ICMP echo requests to the specified host and measure the round-trip time. By default, the script sends 4 packets to the host and waits up to 2 seconds for a response. If a response is received, the script prints the average round-trip time to the console. If no response is received, the script prints a message indicating that the ping failed.

If the -v or --verbose option is specified, the script also prints the minimum, maximum, and average round-trip times to the console.

If the -c <count> or --count <count> option is specified with a value greater than 1, the script will run continuously and send the specified number of packets at the specified interval using the -i <interval> or --interval <interval> option. The script will only exit if an error occurs or the user interrupts the script using Ctrl+C.

If the ping fails with an IPv4 address, the script automatically switches to an IPv6 address to retry the ping.

# Why it's useful
The ping script can be useful for troubleshooting network connectivity issues. By pinging a remote host, you can quickly determine if your computer is able to communicate with the host and how long it takes for packets to travel between your computer and the host. This information can help you diagnose problems with your network connection and identify potential bottlenecks or issues with the remote host.