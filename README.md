# Storing Passwords Quiz
## Would you like salt with your hash?


With your partner, in words both of you will understand 6 months from now, answer the following questions.

> A customer hires you to consult on a web app.  You notice that they are storing their passwords in plaintext.  What advice would you give the customer.  This advice should outline the risks of the current solution, and give a list of best practices for a new solution.

I would not recommend every storing your passwords in plaintext because they are very easy for hackers to access your passwords (and therefore your accounts). This leaves you as an individual open to attacks and/or your company open to liability lawsuits.
We recommend that you use hashing algorithms to store your passwords - with salt as well. This adds a double layer of protection because the hacker must figure out the hashing algorithm for each individual password instead of just having to break one algorithm. We also recommend that you do not add any requirements to password creation that limit the length. Also add some recommendations to the password creation page like 'don't use your birthday, hometown, kidsname, other easily accessible info as your password alone' etc but nothing that give away too much about what the password might be.

> You are tasked for creating a RFP (request for proposal) for a new cryptographic hashing algorithm.  What requirements would you put in place for this new algorithm.

1) no matter how long the password  you put in is, it should always return a hashed string the same length of characters
2) the algorithm can only go one way
3) add salt to the password before creating the hash
4) do not store the password itself - the salt will be stored, but not the password
5) make sure that no two passwords result in the same hash (no collision)
6) make sure the if two passwords are very similar, they have very different hashes - minor changes in the passwords make major differences in the hashes
