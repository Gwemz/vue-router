<template>
  <div id="app">
    <img src="data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiIHN0YW5kYWxvbmU9Im5vIj8+Cjxzdmcgd2lkdGg9IjE0NnB4IiBoZWlnaHQ9IjM4cHgiIHZpZXdCb3g9IjAgMCAxNDYgMzgiIHZlcnNpb249IjEuMSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIiB4bWxuczp4bGluaz0iaHR0cDovL3d3dy53My5vcmcvMTk5OS94bGluayI+CiAgICA8IS0tIEdlbmVyYXRvcjogU2tldGNoIDQwICgzMzc2MikgLSBodHRwOi8vd3d3LmJvaGVtaWFuY29kaW5nLmNvbS9za2V0Y2ggLS0+CiAgICA8dGl0bGU+U2hhcGUgQ29weTwvdGl0bGU+CiAgICA8ZGVzYz5DcmVhdGVkIHdpdGggU2tldGNoLjwvZGVzYz4KICAgIDxkZWZzPjwvZGVmcz4KICAgIDxnIGlkPSJ2Mi4yLjAiIHN0cm9rZT0ibm9uZSIgc3Ryb2tlLXdpZHRoPSIxIiBmaWxsPSJub25lIiBmaWxsLXJ1bGU9ImV2ZW5vZGQiPgogICAgICAgIDxnIGlkPSLpppbpobUt6buY6K6k5pWI5p6cLWNvcHktMiIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoLTcwLjAwMDAwMCwgLTE5LjAwMDAwMCkiIGZpbGw9IiM0MDlFRkYiPgogICAgICAgICAgICA8cGF0aCBkPSJNMjEyLjEzNTQ0MSw0NS4xNTc4MDc3IEMyMTIuMTM1NDQxLDQ1LjE1NzgwNzcgMjEyLjQyMDIzNyw0NS4xNTA1MTA1IDIxMi45NjA5MzcsNDUuMTU3ODA3NyBDMjEzLjUwMTYzNyw0NS4xNjUxMDQ5IDIxMy42NDg4NTEsNDUuNTcwODU1NiAyMTMuNjQ4ODUxLDQ1LjU3MDg1NTYgQzIxMy42NDg4NTEsNDUuNTcwODU1NiAyMTQuNzMzODI4LDQ3LjU2NjU2NTcgMjE1LjAyNDY3Nyw0OC4wNDkxNDM0IEMyMTUuMjgzNjA4LDQ4LjQ3ODcxMzMgMjE0Ljk3MzIyMSw0OC40NzA4NjU0IDIxNC45MDE4MTYsNDguNDYzODQzNiBDMjE0LjkwMjUwNCw0OC40NjI4Nzk4IDIxNC44ODcwOTUsNDguNDYyMTkxNCAyMTQuODg3MDk1LDQ4LjQ2MjE5MTQgQzIxNC44ODcwOTUsNDguNDYyMTkxNCAyMTQuODkzMDExLDQ4LjQ2MzAxNzUgMjE0LjkwMTgxNiw0OC40NjM4NDM2IEMyMTQuODk4NjUyLDQ4LjQ2ODI0OTUgMjE0LjU5NDczMSw0OC40NzgzMDAzIDIxMS40NDc1MjgsNDguNDYyMTkxNCBDMjA3LjA1ODY0MSw0Ny44NjY1NzYyIDIwNi45MDczLDQzLjkxODY2MzggMjA2LjkwNzMsNDMuOTE4NjYzOCBMMjA2LjkwNzMsMzYuODk2ODQ4MyBMMjA0LjQzMDgxMiwzNi44OTY4NDgzIEwyMDQuNDMwODEyLDM0LjI4MDg3NzkgQzIwNC40MzA4MTIsMzMuOTI0Mjc5OCAyMDQuODQzNTYsMzMuODY3ODI5OSAyMDQuODQzNTYsMzMuODY3ODI5OSBMMjA2LjkwNzMsMzMuODY3ODI5OSBMMjA2LjkwNzMsMzEuMjUxODU5NCBDMjA2LjkwNzMsMzAuODI1MTgwOSAyMDcuMzIwMDQ4LDMwLjcwMTEyODggMjA3LjMyMDA0OCwzMC43MDExMjg4IEMyMDcuMzIwMDQ4LDMwLjcwMTEyODggMjA4Ljc3MjY0NiwzMC4yODU4Nzc5IDIwOS42MTc4MTYsMzAuMDQ0MTA3MiBDMjA5Ljk2NDY2MiwyOS45NDQ5NzU2IDIxMC4wNzE3MDEsMzAuMTUwMzk4MiAyMTAuMDcxNzAxLDMwLjE1MDM5ODIgQzIxMC4wNzE3MDEsMzAuMTUwMzk4MiAyMTAuMjA5Mjg0LDMwLjA3NzQyNjQgMjEwLjIwOTI4NCwzMC4zOTI3MTk2IEwyMTAuMjA5Mjg0LDM0LjAwNTUxMjUgTDIxMy43ODY0MzMsMzQuMDA1NTEyNSBDMjE0LjEzNDY1NSwzNC4wMDU1MTI1IDIxNC4xOTkxODEsMzQuNDE4NTYwNSAyMTQuMTk5MTgxLDM0LjQxODU2MDUgTDIxNC4xOTkxODEsMzcuMDM0NTMxIEwyMTAuMjA5Mjg0LDM3LjAzNDUzMSBMMjEwLjIwOTI4NCw0My4wOTI1Njc4IEMyMTAuMjA5Mjg0LDQ0Ljg1MzM5MTMgMjEyLjEzNTQ0MSw0NS4xNTc4MDc3IDIxMi4xMzU0NDEsNDUuMTU3ODA3NyBMMjEyLjEzNTQ0MSw0NS4xNTc4MDc3IFogTTIwMS41NDE1NzYsNDguMTg2ODI2MSBMMTk5LjM0MDI1Myw0OC4xODY4MjYxIEMxOTguOTA4MzgxLDQ4LjE4NjgyNjEgMTk4LjkyNzUwNSw0Ny42MzYwOTU1IDE5OC45Mjc1MDUsNDcuNjM2MDk1NSBMMTk4LjkyNzUwNSwzNy40NDc1Nzg5IEMxOTguOTI3NTA1LDM2LjgyODY5NTQgMTk4LjEwMjAwOSwzNi42MjE0ODMgMTk4LjEwMjAwOSwzNi42MjE0ODMgTDE5My41NjE3ODEsMzYuNjIxNDgzIEMxOTIuODg0NDYyLDM2LjYyMTQ4MyAxOTIuODczODY4LDM3LjQ0NzU3ODkgMTkyLjg3Mzg2OCwzNy40NDc1Nzg5IEwxOTIuODczODY4LDQ3Ljc3Mzc3ODEgQzE5Mi44NzM4NjgsNDguMTc4NzAyOCAxOTIuNDYxMTIsNDguMTg2ODI2MSAxOTIuNDYxMTIsNDguMTg2ODI2MSBMMTkwLjI1OTc5Nyw0OC4xODY4MjYxIEMxODkuNzc1NzgyLDQ4LjE4NjgyNjEgMTg5Ljg0NzA0OSw0Ny42MzYwOTU1IDE4OS44NDcwNDksNDcuNjM2MDk1NSBMMTg5Ljg0NzA0OSwzNC44MzE2MDg1IEMxODkuODQ3MDQ5LDMzLjgwMzExOSAxOTEuMDg1MjkzLDMzLjU5MjQ2NDYgMTkxLjA4NTI5MywzMy41OTI0NjQ2IEwyMDAuNzE2MDgsMzMuNTkyNDY0NiBDMjAxLjY3Nzc4MywzMy41OTI0NjQ2IDIwMS45NTQzMjQsMzQuODMxNjA4NSAyMDEuOTU0MzI0LDM0LjgzMTYwODUgTDIwMS45NTQzMjQsNDcuNDk4NDEyOCBDMjAxLjk1NDMyNCw0OC4yMTg2MzA4IDIwMS41NDE1NzYsNDguMTg2ODI2MSAyMDEuNTQxNTc2LDQ4LjE4NjgyNjEgTDIwMS41NDE1NzYsNDguMTg2ODI2MSBaIE0xODUuODU3MTUyLDQyLjQwNDE1NDYgTDE3Ny4zMjcwMjcsNDIuNDA0MTU0NiBMMTc3LjMyNzAyNyw0NC40NjkzOTQ0IEMxNzcuMzI3MDI3LDQ1LjIxMzU2OTEgMTc4LjI5MDEwNiw0NS40MzMxNzMgMTc4LjI5MDEwNiw0NS40MzMxNzMgTDE4NS4xNjkyMzksNDUuNDMzMTczIEMxODUuNjU4NzU4LDQ1LjQzMzE3MyAxODUuOTk0NzM1LDQ1Ljg0NjIyMSAxODUuOTk0NzM1LDQ1Ljg0NjIyMSBDMTg1Ljk5NDczNSw0NS44NDYyMjEgMTg2LjU5NTAwOCw0Ny4wOTUxNDAzIDE4Ni44MjAyMzEsNDcuNjM2MDk1NSBDMTg3LjA0NTQ1NCw0OC4xNzcwNTA2IDE4Ni40MDc0ODMsNDguMTg2ODI2MSAxODYuNDA3NDgzLDQ4LjE4NjgyNjEgTDE3Ni4wODg3ODMsNDguMTg2ODI2MSBDMTc0Ljg0NjEzNiw0OC4xODY4MjYxIDE3NC41NzUzNzQsNDYuNjcyMzE2OSAxNzQuNTc1Mzc0LDQ2LjY3MjMxNjkgTDE3NC41NzUzNzQsMzQuOTY5MjkxMSBDMTc0LjU3NTM3NCwzNC4yOTYyOTgzIDE3NS41Mzg0NTIsMzQuMDA1NTEyNSAxNzUuNTM4NDUyLDM0LjAwNTUxMjUgTDE4NS44NTcxNTIsMzQuMDA1NTEyNSBDMTg2Ljg5NDExMywzNC4wMDU1MTI1IDE4Ny4wOTUzOTYsMzUuMjQ0NjU2NCAxODcuMDk1Mzk2LDM1LjI0NDY1NjQgTDE4Ny4wOTUzOTYsNDEuMTY1MDEwNyBDMTg3LjA5NTM5Niw0Mi4xNjM4OTgzIDE4NS44NTcxNTIsNDIuNDA0MTU0NiAxODUuODU3MTUyLDQyLjQwNDE1NDYgTDE4NS44NTcxNTIsNDIuNDA0MTU0NiBaIE0xODQuMzQzNzQzLDM3LjQ0NzU3ODkgQzE4NC4zNDM3NDMsMzcuNDQ3NTc4OSAxODQuMjU3MDY2LDM2Ljc1OTE2NTcgMTgzLjY1NTgzLDM2Ljc1OTE2NTcgTDE3OC4wMTQ5NCwzNi43NTkxNjU3IEMxNzguMDE0OTQsMzYuNzU5MTY1NyAxNzcuMzI3MDI3LDM2Ljk0Mzc5ODEgMTc3LjMyNzAyNywzNy40NDc1Nzg5IEwxNzcuMzI3MDI3LDM4Ljk2MjA4ODIgQzE3Ny4zMjcwMjcsMzguOTYyMDg4MiAxNzcuMzQ2ODM5LDM5LjY1MDUwMTQgMTc4LjAxNDk0LDM5LjY1MDUwMTQgTDE4My42NTU4MywzOS42NTA1MDE0IEMxODMuNjU1ODMsMzkuNjUwNTAxNCAxODQuMzQzNzQzLDM5LjQ4MDQ2MzQgMTg0LjM0Mzc0MywzOC44MjQ0MDU1IEwxODQuMzQzNzQzLDM3LjQ0NzU3ODkgTDE4NC4zNDM3NDMsMzcuNDQ3NTc4OSBaIE0xNzEuNDEwOTcyLDQ4LjE4NjgyNjEgTDE2OS4yMDk2NSw0OC4xODY4MjYxIEMxNjguOTE5MjEzLDQ4LjE4NjgyNjEgMTY4Ljc5NjkwMiw0Ny43NzM3NzgxIDE2OC43OTY5MDIsNDcuNzczNzc4MSBMMTY4Ljc5NjkwMiwzNy40NDc1Nzg5IEMxNjguNzk2OTAyLDM2LjgwNzIxNjkgMTY3Ljk3MTQwNiwzNi42MjE0ODMgMTY3Ljk3MTQwNiwzNi42MjE0ODMgTDE2NS45MDc2NjYsMzYuNjIxNDgzIEMxNjUuMzMxODgyLDM2LjYyMTQ4MyAxNjUuMjE5NzUyLDM3LjQ0NzU3ODkgMTY1LjIxOTc1MiwzNy40NDc1Nzg5IEwxNjUuMjE5NzUyLDQ3Ljc3Mzc3ODEgQzE2NS4yMTk3NTIsNDguMTE2MzMyNiAxNjQuODA3MDA0LDQ4LjE4NjgyNjEgMTY0LjgwNzAwNCw0OC4xODY4MjYxIEwxNjIuNjA1NjgyLDQ4LjE4NjgyNjEgQzE2Mi4yOTk1Niw0OC4xODY4MjYxIDE2Mi4xOTI5MzQsNDcuNzczNzc4MSAxNjIuMTkyOTM0LDQ3Ljc3Mzc3ODEgTDE2Mi4xOTI5MzQsMzcuNDQ3NTc4OSBDMTYyLjE5MjkzNCwzNi43OTI4OTc5IDE2MS4zNjc0MzgsMzYuNjIxNDgzIDE2MS4zNjc0MzgsMzYuNjIxNDgzIEwxNTkuMzAzNjk4LDM2LjYyMTQ4MyBDMTU4LjY3Mzk4MiwzNi42MjE0ODMgMTU4LjYxNTc4NCwzNy40NDc1Nzg5IDE1OC42MTU3ODQsMzcuNDQ3NTc4OSBMMTU4LjYxNTc4NCw0Ny43NzM3NzgxIEMxNTguNjE1Nzg0LDQ4LjIxNTczOTUgMTU4LjIwMzAzNiw0OC4xODY4MjYxIDE1OC4yMDMwMzYsNDguMTg2ODI2MSBMMTU2LjAwMTcxNCw0OC4xODY4MjYxIEMxNTUuNTg5Mzc4LDQ4LjE4NjgyNjEgMTU1LjU4ODk2Niw0Ny43NzM3NzgxIDE1NS41ODg5NjYsNDcuNzczNzc4MSBMMTU1LjU4ODk2NiwzNC42OTM5MjU4IEMxNTUuNTg4OTY2LDMzLjkzNjI1ODIgMTU2LjY4OTYyNywzMy41OTI0NjQ2IDE1Ni42ODk2MjcsMzMuNTkyNDY0NiBMMTcwLjQ0Nzg5NCwzMy41OTI0NjQ2IEMxNzEuNTUyMjcsMzMuNTkyNDY0NiAxNzEuODIzNzIsMzQuOTY5MjkxMSAxNzEuODIzNzIsMzQuOTY5MjkxMSBMMTcxLjgyMzcyLDQ3Ljc3Mzc3ODEgQzE3MS44MjM3Miw0OC4yNDkzMzQgMTcxLjQxMDk3Miw0OC4xODY4MjYxIDE3MS40MTA5NzIsNDguMTg2ODI2MSBMMTcxLjQxMDk3Miw0OC4xODY4MjYxIFogTTE1MS40NjE0ODYsNDIuNDA0MTU0NiBMMTQyLjkzMTM2LDQyLjQwNDE1NDYgTDE0Mi45MzEzNiw0NC40NjkzOTQ0IEMxNDIuOTMxMzYsNDUuMjEzNTY5MSAxNDMuODk0NDM5LDQ1LjQzMzE3MyAxNDMuODk0NDM5LDQ1LjQzMzE3MyBMMTUwLjc3MzU3Miw0NS40MzMxNzMgQzE1MS4yNjMwOTIsNDUuNDMzMTczIDE1MS41OTkwNjgsNDUuODQ2MjIxIDE1MS41OTkwNjgsNDUuODQ2MjIxIEMxNTEuNTk5MDY4LDQ1Ljg0NjIyMSAxNTIuMTk5MjA0LDQ3LjA5NTE0MDMgMTUyLjQyNDU2NCw0Ny42MzYwOTU1IEMxNTIuNjQ5Nzg3LDQ4LjE3NzA1MDYgMTUyLjAxMTgxNiw0OC4xODY4MjYxIDE1Mi4wMTE4MTYsNDguMTg2ODI2MSBMMTQxLjY5MzExNyw0OC4xODY4MjYxIEMxNDAuNDUwNDcsNDguMTg2ODI2MSAxNDAuMTc5NzA3LDQ2LjY3MjMxNjkgMTQwLjE3OTcwNyw0Ni42NzIzMTY5IEwxNDAuMTc5NzA3LDM0Ljk2OTI5MTEgQzE0MC4xNzk3MDcsMzQuMjk2Mjk4MyAxNDEuMTQyNzg2LDM0LjAwNTUxMjUgMTQxLjE0Mjc4NiwzNC4wMDU1MTI1IEwxNTEuNDYxNDg2LDM0LjAwNTUxMjUgQzE1Mi40OTg0NDYsMzQuMDA1NTEyNSAxNTIuNjk5NzMsMzUuMjQ0NjU2NCAxNTIuNjk5NzMsMzUuMjQ0NjU2NCBMMTUyLjY5OTczLDQxLjE2NTAxMDcgQzE1Mi42OTk3Myw0Mi4xNjM4OTgzIDE1MS40NjE0ODYsNDIuNDA0MTU0NiAxNTEuNDYxNDg2LDQyLjQwNDE1NDYgTDE1MS40NjE0ODYsNDIuNDA0MTU0NiBaIE0xNDkuOTQ4MDc2LDM3LjQ0NzU3ODkgQzE0OS45NDgwNzYsMzcuNDQ3NTc4OSAxNDkuODYxMzk5LDM2Ljc1OTE2NTcgMTQ5LjI2MDE2MywzNi43NTkxNjU3IEwxNDMuNjE5Mjc0LDM2Ljc1OTE2NTcgQzE0My42MTkyNzQsMzYuNzU5MTY1NyAxNDIuOTMxMzYsMzYuOTQzNzk4MSAxNDIuOTMxMzYsMzcuNDQ3NTc4OSBMMTQyLjkzMTM2LDM4Ljk2MjA4ODIgQzE0Mi45MzEzNiwzOC45NjIwODgyIDE0Mi45NTExNzIsMzkuNjUwNTAxNCAxNDMuNjE5Mjc0LDM5LjY1MDUwMTQgTDE0OS4yNjAxNjMsMzkuNjUwNTAxNCBDMTQ5LjI2MDE2MywzOS42NTA1MDE0IDE0OS45NDgwNzYsMzkuNDgwNDYzNCAxNDkuOTQ4MDc2LDM4LjgyNDQwNTUgTDE0OS45NDgwNzYsMzcuNDQ3NTc4OSBMMTQ5Ljk0ODA3NiwzNy40NDc1Nzg5IFogTTEzOC4xMTU5NjcsNDguMTg2ODI2MSBMMTMyLjg4NzgyNiw0OC4xODY4MjYxIEMxMzIuODg3ODI2LDQ4LjE4NjgyNjEgMTI5LjA2MTkyNyw0OC4wMDYxODY1IDEyOC43NjAzNDYsNDQuMTk0MDI5MSBDMTI4Ljc0ODIzOSw0MC4yNzkwMjI4IDEyOC43NjAzNDYsMjguMDg1MTU4MyAxMjguNzYwMzQ2LDI4LjA4NTE1ODMgTDEzMS4yMzY4MzQsMjguMDg1MTU4MyBDMTMxLjIzNjgzNCwyOC4wODUxNTgzIDEzMi4wNjIzMywyOC4wNzAxNTA5IDEzMi4wNjIzMywyOC45MTEyNTQzIEwxMzIuMDYyMzMsNDMuMzY3OTMzMSBDMTMyLjA2MjMzLDQzLjM2NzkzMzEgMTMyLjM1MDAxNSw0NC41NjM4NDQ3IDEzMy45ODg0ODcsNDUuMDIwMTI1IEMxMzUuODM5OCw0NS4wMTA3NjI2IDEzNi4xODk4MSw0NS4wMjAxMjUgMTM2LjE4OTgxLDQ1LjAyMDEyNSBDMTM2LjE4OTgxLDQ1LjAyMDEyNSAxMzYuOTA3MzAzLDQ0Ljc5MDE5NSAxMzcuNDI4MDU0LDQ1LjcwODUzODMgQzEzNy45NDg4MDQsNDYuNjI2ODgxNiAxMzguNTI4NzE1LDQ3LjYzNjA5NTUgMTM4LjUyODcxNSw0Ny42MzYwOTU1IEMxMzguNTI4NzE1LDQ3LjYzNjA5NTUgMTM4LjYxMTU0LDQ4LjE4NjgyNjEgMTM4LjExNTk2Nyw0OC4xODY4MjYxIEwxMzguMTE1OTY3LDQ4LjE4NjgyNjEgWiBNMTExLjU2MjUxMyw0Ny4zNjA3MzAyIEwxMTEuNTYyNTEzLDI5LjE4NjYxOTYgQzExMS41NjI1MTMsMjguMzgwNzYzIDExMi4yNTA0MjYsMjguMjIyODQxIDExMi4yNTA0MjYsMjguMjIyODQxIEwxMjUuMTgzMTk3LDI4LjIyMjg0MSBDMTI1LjkwNjQ2OSwyOC4yMjI4NDEgMTI1LjU5NTk0NSwyOS4wNDg5MzY5IDEyNS41OTU5NDUsMjkuMDQ4OTM2OSBDMTI1LjU5NTk0NSwyOS4wNDg5MzY5IDEyNS4xOTI4MjcsMzAuMTY2MDk0IDEyNC45MDgwMzEsMzAuNzAxMTI4OCBDMTI0LjYyMzIzNSwzMS4yMzYxNjM2IDEyNC4wODI1MzUsMzEuMjUxODU5NCAxMjQuMDgyNTM1LDMxLjI1MTg1OTQgTDExNS42ODk5OTMsMzEuMjUxODU5NCBDMTE0LjkwODUyMywzMS4yNTE4NTk0IDExNC44NjQ0OTcsMzEuOTQwMjcyNyAxMTQuODY0NDk3LDMxLjk0MDI3MjcgTDExNC44NjQ0OTcsMzYuNDgzODAwMyBMMTI0LjM1NzcwMSwzNi40ODM4MDAzIEMxMjQuOTE0NjM1LDM2LjQ4MzgwMDMgMTI0LjYzMjg2NiwzNy4xNzIyMTM2IDEyNC42MzI4NjYsMzcuMTcyMjEzNiBDMTI0LjYzMjg2NiwzNy4xNzIyMTM2IDEyMy45MjE4MzksMzguNjg4OTI1OCAxMjMuNjY5Nzg3LDM5LjA5OTc3MDggQzEyMy40MTc3MzYsMzkuNTEwNjE1OSAxMjIuODQ0MjkxLDM5LjUxMjgxODggMTIyLjg0NDI5MSwzOS41MTI4MTg4IEwxMTQuODY0NDk3LDM5LjUxMjgxODggTDExNC44NjQ0OTcsNDQuMzMxNzExNyBDMTE0Ljg2NDQ5Nyw0NC45ODg0NTggMTE1LjU1MjQxLDQ1LjE1NzgwNzcgMTE1LjU1MjQxLDQ1LjE1NzgwNzcgTDEyNC4zNTc3MDEsNDUuMTU3ODA3NyBDMTI0Ljk5NjIyMiw0NS4xNTc4MDc3IDEyNS4xODMxOTcsNDUuNTcwODU1NiAxMjUuMTgzMTk3LDQ1LjU3MDg1NTYgQzEyNS4xODMxOTcsNDUuNTcwODU1NiAxMjYuMDU1MTk2LDQ2LjkzMjM5OTQgMTI2LjQyMTQ0MSw0Ny40OTg0MTI4IEMxMjYuNzg3ODIzLDQ4LjA2NDQyNjIgMTI2LjI4Mzg1OCw0OC4xODY4MjYxIDEyNi4yODM4NTgsNDguMTg2ODI2MSBMMTEyLjM4ODAwOSw0OC4xODY4MjYxIEMxMTEuODE0MTUxLDQ4LjE4NjgyNjEgMTExLjU2MjUxMyw0Ny4zNjA3MzAyIDExMS41NjI1MTMsNDcuMzYwNzMwMiBaIE0xMDMuNDE2NTAyLDQ2LjIxNzU1MTEgQzEwMy40MDcwMDgsNDcuNzk0NTY4MiAxMDIuNTg3ODQxLDQ4LjE0NjM0NzQgMTAyLjU4Nzg0MSw0OC4xNDYzNDc0IEMxMDIuNTg3ODQxLDQ4LjE0NjM0NzQgODguNDUyMDQ3OCw1Ni4zMTQ1MDg3IDg3LjUzMjk5NTYsNTYuODI2Mjc1MSBDODYuNjIyMzM2LDU3LjIxNzE1NjEgODYuMDEzNjcwMyw1Ni44MjYyNzUxIDg2LjAxMzY3MDMsNTYuODI2Mjc1MSBDODYuMDEzNjcwMyw1Ni44MjYyNzUxIDcxLjIyMjU3MDYsNDguMjQ3OTU3MiA3MC42ODI2OTYyLDQ3Ljg3MDg0NDQgQzcwLjE0MjY4NDMsNDcuNDkzNzMxNiA3MC4xMzAxNjQzLDQ2LjkwNjM3NzQgNzAuMTMwMTY0Myw0Ni45MDYzNzc0IEM3MC4xMzAxNjQzLDQ2LjkwNjM3NzQgNzAuMTQ1MDIzMiwyOS45MTk5MTc0IDcwLjEzMDE2NDMsMjkuMTMzMzM2NCBDNzAuMTE1MzA1MywyOC4zNDY2MTc3IDcxLjA5Njk1NzYsMjcuNzU1NTQ2MSA3MS4wOTY5NTc2LDI3Ljc1NTU0NjEgTDg1Ljg3NTUzNzMsMTkuMjEzNDM4NyBDODYuNzg1MzcxNCwxOC43MzMyMDE2IDg3LjY3MTEyODYsMTkuMjEzNDM4NyA4Ny42NzExMjg2LDE5LjIxMzQzODcgQzg3LjY3MTEyODYsMTkuMjEzNDM4NyAxMDAuNzI2NjIzLDI2LjgwMjA5MzcgMTAyLjE3MzQ0MiwyNy42MTc3MjU3IEMxMDMuNTkxNTA3LDI4LjI5MTk1NzcgMTAzLjQxNjUwMiwyOS42ODQzNDI0IDEwMy40MTY1MDIsMjkuNjg0MzQyNCBDMTAzLjQxNjUwMiwyOS42ODQzNDI0IDEwMy40MjUzMDcsNDQuNzUxOTE5MiAxMDMuNDE2NTAyLDQ2LjIxNzU1MTEgTDEwMy40MTY1MDIsNDYuMjE3NTUxMSBaIE05Ny41MTYwMTA1LDI5LjE2OTEzMzkgQzk0LjQ5MDAxNzMsMjcuNDI3NDQ4MyA4Ny4zNjE1ODQyLDIzLjI5NzEwNjMgODcuMzYxNTg0MiwyMy4yOTcxMDYzIEM4Ny4zNjE1ODQyLDIzLjI5NzEwNjMgODYuNjY2MTAzOSwyMi45MjEyMzI2IDg1Ljk1MTc3NDcsMjMuMjk3MTA2MyBMNzQuMzQ4NzQwNiwyOS45ODIxNSBDNzQuMzQ4NzQwNiwyOS45ODIxNSA3My41NzgwMDI1LDMwLjQ0NDkwMTQgNzMuNTg5Njk3LDMxLjA2MDQ4MDUgQzczLjYwMTM5MTUsMzEuNjc2MDU5NyA3My41ODk2OTcsNDQuOTY5ODcwOCA3My41ODk2OTcsNDQuOTY5ODcwOCBDNzMuNTg5Njk3LDQ0Ljk2OTg3MDggNzMuNTk5NDY1NCw0NS40Mjk1OTMyIDc0LjAyMzQ5NTEsNDUuNzI0NjQ3MiBDNzQuNDQ3Mzg3Myw0Ni4wMTk3MDExIDg2LjA2MDE4OTgsNTIuNzMzMjQ1MSA4Ni4wNjAxODk4LDUyLjczMzI0NTEgQzg2LjA2MDE4OTgsNTIuNzMzMjQ1MSA4Ni41MzgxNTIsNTMuMDM5MTc1OSA4Ny4yNTMwMzE1LDUyLjczMzI0NTEgQzg3Ljk3NDY1MjYsNTIuMzMyNzI2MiA5OS4wNzMwMzM1LDQ1Ljk0MDI1ODIgOTkuMDczMDMzNSw0NS45NDAyNTgyIEM5OS4wNzMwMzM1LDQ1Ljk0MDI1ODIgOTkuNzE2MjMyNSw0NS42NjQ4OTI5IDk5LjcyMzY2MTksNDQuNDMwNzA1NiBDOTkuNzI1NzI1Nyw0NC4wNzQ3OTU5IDk5LjcyNjU1MTIsNDIuNjkzMjg4MSA5OS43MjY2ODg3LDQwLjk1NzUyMjkgTDg2LjY2MDA1MDIsNDguODc1MjM5NCBMODYuNjYwMDUwMiw0NS44NDYyMjEgQzg2LjY2MDA1MDIsNDQuNjAyMTIwNSA4Ny42MjMxMjg5LDQzLjc4MDk4MTEgODcuNjIzMTI4OSw0My43ODA5ODExIEw5OS4xODA3NjA3LDM2LjgxNjU3OTMgQzk5LjYxNjg5NzgsMzYuMzYxMTI1MSA5OS43MDY4NzY4LDM1LjYzMTU0NDcgOTkuNzI1NDUwNSwzNS4zNTU2Mjg3IEM5OS43MjUwMzc4LDM0LjA5MDQ2MjcgOTkuNzI0NDg3NCwzMi45ODUyODQxIDk5LjcyNDA3NDcsMzIuMjg1MTY3OCBMODYuNjYwMDUwMiw0MC4yMDEyMzIxIEw4Ni42NjAwNTAyLDM3LjAzNDUzMSBDODYuNjYwMDUwMiwzNS43OTA0MzA1IDg3LjQ4NTU0NjIsMzUuMjQ0NjU2NCA4Ny40ODU1NDYyLDM1LjI0NDY1NjQgTDk3LjUxNjAxMDUsMjkuMTY5MTMzOSBaIiBpZD0iU2hhcGUtQ29weSI+PC9wYXRoPgogICAgICAgIDwvZz4KICAgIDwvZz4KPC9zdmc+">
    <div>
      <el-button @click="startHacking">Start</el-button>
    </div>
    <div>

    <!-- fade 淡入淡出 -->
    <h2>fade 淡入淡出</h2>
    <el-button @click="show = !show">Click Me</el-button>

    <div style="display: flex; margin-top: 20px; height: 100px;">
      <transition name="el-fade-in-linear">
        <div v-show="show" class="transition-box">.el-fade-in-linear</div>
      </transition>
      <transition name="el-fade-in">
        <div v-show="show" class="transition-box">.el-fade-in</div>
      </transition>
    </div>
  </div>
  <!-- zoom 缩放 -->
  <h2>zoom 缩放</h2>
  <div>
    <el-button @click="show2 = !show2">Click Me</el-button>

    <div style="display: flex; margin-top: 20px; height: 100px;">
      <transition name="el-zoom-in-center">
        <div v-show="show2" class="transition-box">.el-zoom-in-center</div>
      </transition>

      <transition name="el-zoom-in-top">
        <div v-show="show2" class="transition-box">.el-zoom-in-top</div>
      </transition>

      <transition name="el-zoom-in-bottom">
        <div v-show="show2" class="transition-box">.el-zoom-in-bottom</div>
      </transition>
    </div>
  </div>
  <!-- collapse 展开折叠 -->
  <h2>collapse 展开折叠</h2>
  <div>
    <el-button @click="show3 = !show3">Click Me</el-button>

    <div style="margin-top: 20px; height: 200px;">
      <el-collapse-transition>
        <div v-show="show3">
          <div class="transition-box">el-collapse-transition</div>
          <div class="transition-box">el-collapse-transition</div>
        </div>
      </el-collapse-transition>
    </div>
  </div>

  <!-- layout 基础布局 -->
  <h2>layout 基础布局</h2>
    <el-row>
      <el-col :span="24"><div class="grid-content bg-purple-dark"></div></el-col>
    </el-row>
    <el-row>
      <el-col :span="12"><div class="grid-content bg-purple"></div></el-col>
      <el-col :span="12"><div class="grid-content bg-purple-light"></div></el-col>
    </el-row>
    <el-row>
      <el-col :span="8"><div class="grid-content bg-purple"></div></el-col>
      <el-col :span="8"><div class="grid-content bg-purple-light"></div></el-col>
      <el-col :span="8"><div class="grid-content bg-purple"></div></el-col>
    </el-row>
    <el-row>
      <el-col :span="6"><div class="grid-content bg-purple"></div></el-col>
      <el-col :span="6"><div class="grid-content bg-purple-light"></div></el-col>
      <el-col :span="6"><div class="grid-content bg-purple"></div></el-col>
      <el-col :span="6"><div class="grid-content bg-purple-light"></div></el-col>
    </el-row>
    <el-row>
      <el-col :span="4"><div class="grid-content bg-purple"></div></el-col>
      <el-col :span="4"><div class="grid-content bg-purple-light"></div></el-col>
      <el-col :span="4"><div class="grid-content bg-purple"></div></el-col>
      <el-col :span="4"><div class="grid-content bg-purple-light"></div></el-col>
      <el-col :span="4"><div class="grid-content bg-purple"></div></el-col>
      <el-col :span="4"><div class="grid-content bg-purple-light"></div></el-col>
    </el-row>
    <!-- 分栏间隔 -->
    <h2>分栏间隔</h2>
    <el-row :gutter="20">
      <el-col :span="6"><div class="grid-content bg-purple"></div></el-col>
      <el-col :span="6"><div class="grid-content bg-purple"></div></el-col>
      <el-col :span="6"><div class="grid-content bg-purple"></div></el-col>
      <el-col :span="6"><div class="grid-content bg-purple"></div></el-col>
    </el-row>
    <h2>对齐方式</h2>
    <el-row type="flex" class="row-bg">
      <el-col :span="6"><div class="grid-content bg-purple"></div></el-col>
      <el-col :span="6"><div class="grid-content bg-purple-light"></div></el-col>
      <el-col :span="6"><div class="grid-content bg-purple"></div></el-col>
    </el-row>
    <el-row type="flex" class="row-bg" justify="center">
      <el-col :span="6"><div class="grid-content bg-purple"></div></el-col>
      <el-col :span="6"><div class="grid-content bg-purple-light"></div></el-col>
      <el-col :span="6"><div class="grid-content bg-purple"></div></el-col>
    </el-row>
    <el-row type="flex" class="row-bg" justify="end">
      <el-col :span="6"><div class="grid-content bg-purple"></div></el-col>
      <el-col :span="6"><div class="grid-content bg-purple-light"></div></el-col>
      <el-col :span="6"><div class="grid-content bg-purple"></div></el-col>
    </el-row>
    <el-row type="flex" class="row-bg" justify="space-between">
      <el-col :span="6"><div class="grid-content bg-purple"></div></el-col>
      <el-col :span="6"><div class="grid-content bg-purple-light"></div></el-col>
      <el-col :span="6"><div class="grid-content bg-purple"></div></el-col>
    </el-row>
    <el-row type="flex" class="row-bg" justify="space-around">
      <el-col :span="6"><div class="grid-content bg-purple"></div></el-col>
      <el-col :span="6"><div class="grid-content bg-purple-light"></div></el-col>
      <el-col :span="6"><div class="grid-content bg-purple"></div></el-col>
    </el-row>
    <h2>响应式布局</h2>
    <el-row :gutter="10">
      <el-col :xs="8" :sm="6" :md="4" :lg="3" :xl="1"><div class="grid-content bg-purple"></div></el-col>
      <el-col :xs="4" :sm="6" :md="8" :lg="9" :xl="11"><div class="grid-content bg-purple-light"></div></el-col>
      <el-col :xs="4" :sm="6" :md="8" :lg="9" :xl="11"><div class="grid-content bg-purple"></div></el-col>
      <el-col :xs="8" :sm="6" :md="4" :lg="3" :xl="1"><div class="grid-content bg-purple-light"></div></el-col>
    </el-row>
    <h2>常见页面布局</h2>
    <el-container>
      <el-header>Header</el-header>
      <el-main>Main</el-main>
    </el-container>

    <el-container>
      <el-header>Header</el-header>
      <el-main>Main</el-main>
      <el-footer>Footer</el-footer>
    </el-container>

    <el-container>
      <el-aside width="200px">Aside</el-aside>
      <el-main>Main</el-main>
    </el-container>

    <el-container>
      <el-header>Header</el-header>
      <el-container>
        <el-aside width="200px">Aside</el-aside>
        <el-main>Main</el-main>
      </el-container>
    </el-container>

    <el-container>
      <el-header>Header</el-header>
      <el-container>
        <el-aside width="200px">Aside</el-aside>
        <el-container>
          <el-main>Main</el-main>
          <el-footer>Footer</el-footer>
        </el-container>
      </el-container>
    </el-container>

    <el-container>
      <el-aside width="200px">Aside</el-aside>
      <el-container>
        <el-header>Header</el-header>
        <el-main>Main</el-main>
      </el-container>
    </el-container>

    <el-container>
      <el-aside width="200px">Aside</el-aside>
      <el-container>
        <el-header>Header</el-header>
        <el-main>Main</el-main>
        <el-footer>Footer</el-footer>
      </el-container>
    </el-container>
    <h3>示例</h3>
    <el-container style="height: 500px; border: 1px solid #eee">
  <el-aside width="200px" style="background-color: rgb(238, 241, 246)">
    <el-menu :default-openeds="['1', '3']">
      <el-submenu index="1">
        <template slot="title"><i class="el-icon-message"></i>导航一</template>
        <el-menu-item-group>
          <template slot="title">分组一</template>
          <el-menu-item index="1-1">选项1</el-menu-item>
          <el-menu-item index="1-2">选项2</el-menu-item>
        </el-menu-item-group>
        <el-menu-item-group title="分组2">
          <el-menu-item index="1-3">选项3</el-menu-item>
        </el-menu-item-group>
        <el-submenu index="1-4">
          <template slot="title">选项4</template>
          <el-menu-item index="1-4-1">选项4-1</el-menu-item>
        </el-submenu>
      </el-submenu>
      <el-submenu index="2">
        <template slot="title"><i class="el-icon-menu"></i>导航二</template>
        <el-menu-item-group>
          <template slot="title">分组一</template>
          <el-menu-item index="2-1">选项1</el-menu-item>
          <el-menu-item index="2-2">选项2</el-menu-item>
        </el-menu-item-group>
        <el-menu-item-group title="分组2">
          <el-menu-item index="2-3">选项3</el-menu-item>
        </el-menu-item-group>
        <el-submenu index="2-4">
          <template slot="title">选项4</template>
          <el-menu-item index="2-4-1">选项4-1</el-menu-item>
        </el-submenu>
      </el-submenu>
      <el-submenu index="3">
        <template slot="title"><i class="el-icon-setting"></i>导航三</template>
        <el-menu-item-group>
          <template slot="title">分组一</template>
          <el-menu-item index="3-1">选项1</el-menu-item>
          <el-menu-item index="3-2">选项2</el-menu-item>
        </el-menu-item-group>
        <el-menu-item-group title="分组2">
          <el-menu-item index="3-3">选项3</el-menu-item>
        </el-menu-item-group>
        <el-submenu index="3-4">
          <template slot="title">选项4</template>
          <el-menu-item index="3-4-1">选项4-1</el-menu-item>
        </el-submenu>
      </el-submenu>
    </el-menu>
  </el-aside>
  
  <el-container>
    <el-header style="text-align: right; font-size: 12px">
      <el-dropdown>
        <i class="el-icon-setting" style="margin-right: 15px"></i>
        <el-dropdown-menu slot="dropdown">
          <el-dropdown-item>查看</el-dropdown-item>
          <el-dropdown-item>新增</el-dropdown-item>
          <el-dropdown-item>删除</el-dropdown-item>
        </el-dropdown-menu>
      </el-dropdown>
      <span>王小虎</span>
    </el-header>
    
    <el-main>
      <el-table >
        <el-table-column prop="date" label="日期" width="140">
        </el-table-column>
        <el-table-column prop="name" label="姓名" width="120">
        </el-table-column>
        <el-table-column prop="address" label="地址">
        </el-table-column>
      </el-table>
    </el-main>
  </el-container>
</el-container>
  <el-button class="bg-blue">Blue</el-button>
  <h2>Icon图标</h2>
  <i class="el-icon-edit"></i>
  <i class="el-icon-share"></i>
  <i class="el-icon-delete"></i>
  <el-button type="primary" icon="el-icon-search">搜索</el-button>
  <h2>Button按钮</h2>
  <div>
    <el-button>默认按钮</el-button>
    <el-button type="primary">主要按钮</el-button>
    <el-button type="success">成功按钮</el-button>
    <el-button type="info">信息按钮</el-button>
    <el-button type="warning">警告按钮</el-button>
    <el-button type="danger">危险按钮</el-button>
  </div>

  <div style="margin: 20px 0">
    <el-button plain>朴素按钮</el-button>
    <el-button type="primary" plain>主要按钮</el-button>
    <el-button type="success" plain>成功按钮</el-button>
    <el-button type="info" plain>信息按钮</el-button>
    <el-button type="warning" plain>警告按钮</el-button>
    <el-button type="danger" plain>危险按钮</el-button>
  </div>

  <div>
    <el-button round>圆形按钮</el-button>
    <el-button type="primary" round>主要按钮</el-button>
    <el-button type="success" round>成功按钮</el-button>
    <el-button type="info" round>信息按钮</el-button>
    <el-button type="warning" round>警告按钮</el-button>
    <el-button type="danger" round>危险按钮</el-button>
  </div>
  <h2>按钮禁用状态</h2>
  <div>
  <el-button disabled>默认按钮</el-button>
  <el-button type="primary" disabled>主要按钮</el-button>
  <el-button type="success" disabled>成功按钮</el-button>
  <el-button type="info" disabled>信息按钮</el-button>
  <el-button type="warning" disabled>警告按钮</el-button>
  <el-button type="danger" disabled>危险按钮</el-button>
</div>

<div style="margin-top: 20px">
  <el-button plain disabled>朴素按钮</el-button>
  <el-button type="primary" plain disabled>主要按钮</el-button>
  <el-button type="success" plain disabled>成功按钮</el-button>
  <el-button type="info" plain disabled>信息按钮</el-button>
  <el-button type="warning" plain disabled>警告按钮</el-button>
  <el-button type="danger" plain disabled>危险按钮</el-button>
</div>
  <h2>文字按钮</h2>
  <el-button type="text">文字按钮</el-button>
  <el-button type="text" disabled>文字按钮</el-button>
  <h3>图标按钮</h3>
  <el-button type="primary" icon="el-icon-edit"></el-button>
  <el-button type="primary" icon="el-icon-share"></el-button>
  <el-button type="primary" icon="el-icon-delete"></el-button>
  <el-button type="primary" icon="el-icon-search">搜索</el-button>
  <el-button type="primary">上传<i class="el-icon-upload el-icon--right"></i></el-button>

  <el-button-group>
    <el-button type="primary" icon="el-icon-arrow-left">上一页</el-button>
    <el-button type="primary">下一页<i class="el-icon-arrow-right el-icon--right"></i></el-button>
  </el-button-group>
  <el-button-group>
    <el-button type="primary" icon="el-icon-edit"></el-button>
    <el-button type="primary" icon="el-icon-share"></el-button>
    <el-button type="primary" icon="el-icon-delete"></el-button>
  </el-button-group>
  <el-button type="primary" :loading="true">加载中</el-button>
  <el-radio v-model="radio" label="1">备选项</el-radio>
  <el-radio v-model="radio" label="2">备选项</el-radio>
  <h3>按钮样式</h3>  
  <div>
    <el-radio-group v-model="radio3">
      <el-radio-button label="上海"></el-radio-button>
      <el-radio-button label="北京"></el-radio-button>
      <el-radio-button label="广州"></el-radio-button>
      <el-radio-button label="深圳"></el-radio-button>
    </el-radio-group>
  </div>
  <div style="margin-top: 20px">
    <el-radio-group v-model="radio4" size="medium">
      <el-radio-button label="上海" ></el-radio-button>
      <el-radio-button label="北京"></el-radio-button>
      <el-radio-button label="广州"></el-radio-button>
      <el-radio-button label="深圳"></el-radio-button>
    </el-radio-group>
  </div>
  <div style="margin-top: 20px">
    <el-radio-group v-model="radio5" size="small">
      <el-radio-button label="上海"></el-radio-button>
      <el-radio-button label="北京" disabled ></el-radio-button>
      <el-radio-button label="广州"></el-radio-button>
      <el-radio-button label="深圳"></el-radio-button>
    </el-radio-group>
  </div>
  <div style="margin-top: 20px">
    <el-radio-group v-model="radio6" disabled size="mini">
      <el-radio-button label="上海"></el-radio-button>
      <el-radio-button label="北京"></el-radio-button>
      <el-radio-button label="广州"></el-radio-button>
      <el-radio-button label="深圳"></el-radio-button>
    </el-radio-group>
  </div>
  <!-- Slider 滑块 -->
  <h3>Slider 滑块</h3>
  <div class="block">
    <span class="demonstration">默认</span>
    <el-slider v-model="value1"></el-slider>
  </div>
  <div class="block">
    <span class="demonstration">自定义初始值</span>
    <el-slider v-model="value2"></el-slider>
  </div>
  <div class="block">
    <span class="demonstration">隐藏 Tooltip</span>
    <el-slider v-model="value3" :show-tooltip="false"></el-slider>
  </div>
  <div class="block">
    <span class="demonstration">格式化 Tooltip</span>
    <el-slider v-model="value4" :format-tooltip="formatTooltip"></el-slider>
  </div>
  <div class="block">
    <span class="demonstration">禁用</span>
    <el-slider v-model="value5" disabled></el-slider>
  </div>
  <h3>Cascader 级联选择器</h3>
  <div class="block">
    <span class="demonstration">默认 click 触发子菜单</span>
    <el-cascader
      :options="options"
      v-model="selectedOptions"
      @change="handleChange">
    </el-cascader>
  </div>
  <div class="block">
    <span class="demonstration">hover 触发子菜单</span>
    <el-cascader
      expand-trigger="hover"
      :options="options"
      v-model="selectedOptions2"
      @change="handleChange">
    </el-cascader>
  </div>

  <h3>Switch开关</h3>
  <el-switch
    v-model="value2"
    active-color="#13ce66"
    inactive-color="#ff4949">
  </el-switch>

  <div>
    <el-switch
    v-model="value3"
    active-text="按月付费"
    inactive-text="按年付费">
    </el-switch>
    <el-switch
      style="display: block"
      v-model="value4"
      active-color="#13ce66"
      inactive-color="#ff4949"
      active-text="按月付费"
      inactive-text="按年付费">
    </el-switch>
  </div>
    <h2>时间选择器</h2>
    <el-time-picker
    v-model="value2"
    :picker-options="{
      selectableRange: '18:30:00 - 20:30:00'
    }"
    placeholder="任意时间点">
  </el-time-picker>
  <el-time-picker
    arrow-control
    v-model="value3"
    :picker-options="{
      selectableRange: '18:30:00 - 20:30:00'
    }"
    placeholder="任意时间点">
  </el-time-picker>
  <h3>评分</h3>
  <div class="block">
    <span class="demonstration">默认不区分颜色</span>
    <el-rate v-model="value1"></el-rate>
  </div>
  <div class="block">
    <span class="demonstration">区分颜色</span>
    <el-rate
      v-model="value2"
      :colors="['#99A9BF', '#F7BA2A', '#FF9900']">
    </el-rate>
  </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    show: true,
    show2: true,
    show3: true,
    radio: '1',
    radio3: '上海',
    radio4: '上海',
    radio5: '上海',
    radio6: '上海',
    value1: 0,
    value2: 50,
    value3: 36,
    value4: 48,
    value5: 42,
    options: [{
      value: 'zhinan',
      label: '指南',
      children: [{
        value: 'shejiyuanze',
        label: '设计原则',
        children: [{
          value: 'yizhi',
          label: '一致'
        }, {
          value: 'fankui',
          label: '反馈'
        }, {
          value: 'xiaolv',
          label: '效率'
        }, {
          value: 'kekong',
          label: '可控'
        }]
      }, {
        value: 'daohang',
        label: '导航',
        children: [{
          value: 'cexiangdaohang',
          label: '侧向导航'
        }, {
          value: 'dingbudaohang',
          label: '顶部导航'
        }]
      }]
    }, {
      value: 'zujian',
      label: '组件',
      children: [{
        value: 'basic',
        label: 'Basic',
        children: [{
          value: 'layout',
          label: 'Layout 布局'
        }, {
          value: 'color',
          label: 'Color 色彩'
        }, {
          value: 'typography',
          label: 'Typography 字体'
        }, {
          value: 'icon',
          label: 'Icon 图标'
        }, {
          value: 'button',
          label: 'Button 按钮'
        }]
      }, {
        value: 'form',
        label: 'Form',
        children: [{
          value: 'radio',
          label: 'Radio 单选框'
        }, {
          value: 'checkbox',
          label: 'Checkbox 多选框'
        }, {
          value: 'input',
          label: 'Input 输入框'
        }, {
          value: 'input-number',
          label: 'InputNumber 计数器'
        }, {
          value: 'select',
          label: 'Select 选择器'
        }, {
          value: 'cascader',
          label: 'Cascader 级联选择器'
        }, {
          value: 'switch',
          label: 'Switch 开关'
        }, {
          value: 'slider',
          label: 'Slider 滑块'
        }, {
          value: 'time-picker',
          label: 'TimePicker 时间选择器'
        }, {
          value: 'date-picker',
          label: 'DatePicker 日期选择器'
        }, {
          value: 'datetime-picker',
          label: 'DateTimePicker 日期时间选择器'
        }, {
          value: 'upload',
          label: 'Upload 上传'
        }, {
          value: 'rate',
          label: 'Rate 评分'
        }, {
          value: 'form',
          label: 'Form 表单'
        }]
      }, {
        value: 'data',
        label: 'Data',
        children: [{
          value: 'table',
          label: 'Table 表格'
        }, {
          value: 'tag',
          label: 'Tag 标签'
        }, {
          value: 'progress',
          label: 'Progress 进度条'
        }, {
          value: 'tree',
          label: 'Tree 树形控件'
        }, {
          value: 'pagination',
          label: 'Pagination 分页'
        }, {
          value: 'badge',
          label: 'Badge 标记'
        }]
      }, {
        value: 'notice',
        label: 'Notice',
        children: [{
          value: 'alert',
          label: 'Alert 警告'
        }, {
          value: 'loading',
          label: 'Loading 加载'
        }, {
          value: 'message',
          label: 'Message 消息提示'
        }, {
          value: 'message-box',
          label: 'MessageBox 弹框'
        }, {
          value: 'notification',
          label: 'Notification 通知'
        }]
      }, {
        value: 'navigation',
        label: 'Navigation',
        children: [{
          value: 'menu',
          label: 'NavMenu 导航菜单'
        }, {
          value: 'tabs',
          label: 'Tabs 标签页'
        }, {
          value: 'breadcrumb',
          label: 'Breadcrumb 面包屑'
        }, {
          value: 'dropdown',
          label: 'Dropdown 下拉菜单'
        }, {
          value: 'steps',
          label: 'Steps 步骤条'
        }]
      }, {
        value: 'others',
        label: 'Others',
        children: [{
          value: 'dialog',
          label: 'Dialog 对话框'
        }, {
          value: 'tooltip',
          label: 'Tooltip 文字提示'
        }, {
          value: 'popover',
          label: 'Popover 弹出框'
        }, {
          value: 'card',
          label: 'Card 卡片'
        }, {
          value: 'carousel',
          label: 'Carousel 走马灯'
        }, {
          value: 'collapse',
          label: 'Collapse 折叠面板'
        }]
      }]
    }, {
      value: 'ziyuan',
      label: '资源',
      children: [{
        value: 'axure',
        label: 'Axure Components'
      }, {
        value: 'sketch',
        label: 'Sketch Templates'
      }, {
        value: 'jiaohu',
        label: '组件交互文档'
      }]
    }],
    selectedOptions: [],
    selectedOptions2: [],
    value1:true,
    value2:true,
    value3: true,
    value4: true
  }),
  methods: {
    startHacking() {
      this.$notify({
        title: "It works!",
        type: "success",
        message:
          "We've laid the ground work for you. It's time for you to build something epic!",
        duration: 5000
      });
    },
    formatTooltip(val) {
      return val / 100;
    },
    handleChange(value) {
      console.log(value);
    }
  }

};
</script>

<style>
body {
  font-family: "Helvetica Neue", Helvetica, "PingFang SC", "Hiragino Sans GB",
    "Microsoft YaHei", "微软雅黑", Arial, sans-serif;
}
#app {
  font-family: Helvetica, sans-serif;
  text-align: center;
  width: 1200px;
  margin: 0 auto;
}
#app img {
  width: 400px;
  margin-bottom: 50px;
}
.transition-box {
  margin-bottom: 10px;
  width: 200px;
  height: 100px;
  border-radius: 4px;
  background-color: #409eff;
  text-align: center;
  color: #fff;
  padding: 40px 20px;
  box-sizing: border-box;
  margin-right: 20px;
}
.el-row {
  margin-bottom: 20px;
  &:last-child {
    margin-bottom: 0;
  }
}
.el-col {
  border-radius: 4px;
}
.bg-purple-dark {
  background: #99a9bf;
}
.bg-purple {
  background: #d3dce6;
}
.bg-purple-light {
  background: #e5e9f2;
}
.grid-content {
  border-radius: 4px;
  min-height: 36px;
}
.row-bg {
  padding: 10px 0;
  background-color: #f9fafc;
}
.el-header,
.el-footer {
  background-color: #b3c0d1;
  color: #333;
  text-align: center;
  line-height: 60px;
}

.el-aside {
  background-color: #d3dce6;
  color: #333;
  text-align: center;
  line-height: 200px;
}

.el-main {
  background-color: #e9eef3;
  color: #333;
  text-align: center;
  line-height: 160px;
}

body > .el-container {
  margin-bottom: 40px;
}

.el-container:nth-child(5) .el-aside,
.el-container:nth-child(6) .el-aside {
  line-height: 260px;
}

.el-container:nth-child(7) .el-aside {
  line-height: 320px;
}
</style>
