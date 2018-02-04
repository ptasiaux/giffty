# giffty
giffty let's you organize gifts exchanges between friends, families or colleagues.

It has specific functionalities such as the ability to submit a wishlist to your counterparty, avoid gifts between couples and avoiding loops.

The script allows you to pair and coordinate emails between parties.

First, pairing.py takes a .csv file where the first row contains column headers (ignored), the first column contains time stamps (ignored), and further columns contain the participants' full name, room number (assuming all living in the same building) and email address. It then generates a csv with these columns for 'givers' adjacent to columns for 'receivers', such that:

a person doesn't have to give a gift to himself;
a person doesn't receive a gift from the person he's given a gift to;
a person shouldn't get a gift for a room mate (partner, child, parent);
a person shouldn't give a gift to someone from the same 'room', household or team as his own room mate/team member/partner; and
everyone gets exactly one gift.

Then, sendemail.py sends an email to each 'giver' with information about his 'receiver', corresponding with the list generated in the previous script. Run with caution, as this sends an email to everyone upon running!

Adapted from BrechtDeMan
