## NextJS API---> Response Method

### Object Response
![](https://imgur.com/ZonmeVZ.png)

```bash
import { NextResponse } from "next/server";


export async function GET(request:Request) {

    
    return NextResponse.json(
        {
            Name: "Wasim",
            Email: "mdwasimu015@gmail.com",
            Mobile: "01878594002",
        },
        {status: 200}
    )
}
```
---

### Array Response
![](https://imgur.com/SXgf2Fx.png)

```bash
import { NextResponse } from "next/server";


export async function GET(request:Request) {

    
    return NextResponse.json(
        [
            { Name: "Wasim", Email: "mdwasimu015@gmail.com", Mobile: "01878594002", },
            { Name: "Omar", Email: "mdwasimu015@gmail.com", Mobile: "01878594002", },
            { Name: "Jaber", Email: "mdwasimu015@gmail.com", Mobile: "01878594002", },
            { Name: "Hadi", Email: "mdwasimu015@gmail.com", Mobile: "01878594002", },
            { Name: "Hasnat", Email: "mdwasimu015@gmail.com", Mobile: "01878594002", },
        ],
        {status: 200}
    )
}
```
---
