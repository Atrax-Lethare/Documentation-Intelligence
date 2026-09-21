# Subscription model

We would be using LLMs in order to provide a natural language interface with which the user can interact in order to get the answers for queries.
That would incur API costs. 

We can wrap the access to the inference around a freemium subscription model:
1. **Free tier** - to a limited access such that the user can query upto a limit of tokens of input and output (free session limit).
   We can plan perfectly to limit the context window of outputs to the right level of information to be provided to the user - this would generate lesser API costs
   and also reduce hallucinations, since no unnecessary quantity of information would be generated - basically, the user doesn't have to worry about giving a perfect
   prompt in order to get limited output. Doing this would let us host very generous free tiers as well.
2. **Self-API tier** - the user can use his/her own API key of any LLM, so that he can use that LLM embedded in our system's architecture and freely spend them as much as they want to.
3. **Paid tier** - if the user exceeds the free tier and doesn't have an API key of their own, they can subscribe to our paid tier and pay for any more extensive usage.
   But this tier would not be for profit - it would rather be for covering only the API costs that come by due to excessive usage of the LLM inference by the user.


                                                           FREE TIER
                                                               |
                                        _______________________|_______________________
                                       |                                               |
                                    SELF - API TIER                               PAID TIER

   
