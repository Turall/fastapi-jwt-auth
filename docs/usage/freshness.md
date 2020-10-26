The fresh token pattern is built into this extension. this pattern is very simple, you can choose to mark some access tokens as fresh and other as a non-fresh token, and use the <b>fresh_jwt_required()</b> function to only allow fresh tokens to access the certain endpoint.

This is useful for allowing the fresh token to do some critical things (such as update information user) in real case you can see in the GitHub system when user wants to delete a repository in a certain time you need login if token not fresh again. Utilizing Fresh tokens in conjunction with refresh tokens can lead to a more secure site, without creating a bad user experience by making users constantly re-authenticate.

Here is an example of how you could utilize refresh tokens with the fresh token pattern:

```python
{!../examples/freshness.py!}
```