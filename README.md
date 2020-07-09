# Issue 3973

Run with `python -m SimpleHTTPServer` (or similiar).

## Describe the bug

After updating to 2.10.52 posts are not sorted correctly. 

## To Reproduce

1. Start a webserver: `python -m SimpleHTTPServer`
2. Start a local proxy: `npx netlify-cms-proxy-server`
3. Navigate to localhost:8000/admin
4. Sort posts in descending order
5. Posts are sorted as follows: 2, 1, 3, 4, 5
6. Decrement the version to 2.10.51 in `admin/index.html`
7. Posts are sorted as follows: 5, 4, 3, 2, 1

## Expected behaviour

Posts should be correctly sorted in descending order: 5, 4, 3, 2, 1 (works in 2.10.51)
