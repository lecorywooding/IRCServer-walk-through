# LDW made changes to the config file
# Name of server and its description
# Changed  network name

/*
 * serverinfo {}:  contains information about the server
 */
serverinfo {
	/*
	 * name: the name of this server. This cannot be changed at runtime.
	 */
	name = "Woodhouse.irc";

	/*
	 * sid: a server's unique ID. This is three characters long and must
	 * be in the form [0-9][A-Z0-9][A-Z0-9]. The first character must be
	 * a digit, followed by 2 alpha-numerical letters.
	 *
	 * NOTE: The letters must be capitalized. This cannot be changed at runtime.
	 *
	 * A sid is automatically generated at runtime, if you want to configure
	 * a specific sid, uncomment the following line.
	 */
#	sid = "0HY";

	/*
	 * description: the description of the server.
	 */
	description = "Woodhouses' Pi IRC Server";

	/*
	 * network_name, network_desc: the name and description of the network this
	 * server is on. Shown in the 005 reply and used with serverhiding.
	 */
	network_name = "Woodhouse";
	network_desc = "This is Woodhouses Network";
#
#
#
#

# Changed these settings to limit users


  /*
   * class {}:  contains information about classes for users
   */
   /*
   	 * max_global: network-wide limit of users per ident@host (optional)
   	 */
   	max_global = 10;

   	/*
   	 * max_number: the maximum number of users allowed in this class (optional)
   	 */
   	max_number = 100;

   	/*
#
#
#
#

#operator information changed
#encrypted password required for password block
#encrypted password will be unique per user

#operator {
	/* name: the name of the operator */
	name = "Woodhouse";

	/*
	 * user: the user@host required for this operator. Multiple user
	 * lines are permitted within each operator {} block.
	 */
	user = "*sheep@192.0.2.0/26";
	user = "*@*";

	/*
	 * password: the password required to oper. By default this will need
	 * to be encrypted using the provided mkpasswd tool.
	 * The availability of various password hashing algorithms may vary
	 * depending on the system's crypt(3) implementation.
	 */
	password = "ENCRYPTED PASSWORD GOES HERE";

	/*
	 * encrypted: indicates whether the oper password above has been
	 * encrypted. Default is 'yes' if nothing else is specified.
	 */
	encrypted = yes;

#
#
#
#

#Find this block if your users are having trouble with need_ident
#This is only recommended if users are having trouble

  auth {
	   user = "*@*";
	  class = "users";
#	  flags = need_ident;
