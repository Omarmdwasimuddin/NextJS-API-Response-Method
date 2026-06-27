## NextJS API---> Response Method

### Object Response
![](https://imgur.com/ZonmeVZ.png)

```bash
import { NextRequest, NextResponse } from "next/server";


export async function GET(request:NextRequest) {

    
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
import { NextRequest, NextResponse } from "next/server";


export async function GET(request:NextRequest) {

    
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

### Status Code Response
![](https://imgur.com/erWwCum.png)

```bash
import { NextRequest, NextResponse } from "next/server";


export async function GET(request:Request) {

    
    return NextResponse.json(
        {},
        {status: 400}
    )
}
```
---

### Headers Response
![](https://imgur.com/rC1kYyN.png)

```bash
import { NextRequest, NextResponse } from "next/server";


export async function GET(request:NextRequest) {

    
    return NextResponse.json(
        {},
        {
            status: 200,
            headers:{"token":"abc-123-xyz"}
        }
    )
}
```
---

### Headers Response [multiple value set]
![](https://imgur.com/x0hdpKx.png)

```bash
import { NextRequest, NextResponse } from "next/server";


export async function GET(request:NextRequest) {

    
    return NextResponse.json(
        {},
        {
            status: 200,
            headers:{
                "token":"abc-123-xyz",
                "token2":"eea-014-hello01"
            }
        }
    )
}
```
---

### Cookie Response
![](https://imgur.com/tHl4l6w.png)
![](https://imgur.com/Rnm98UQ.png)

```bash
import { NextRequest, NextResponse } from "next/server";


export async function GET(request:NextRequest) {

    
    return NextResponse.json(
        {},
        {
            status: 200,
            headers:{
                "token":"abc-123-xyz",
                "token2":"eea-014-hello01",
                "Set-Cookie":"Auth=123;Path=/;"
            }
        }
    )
}
```
---

### Redirect Response
![](https://imgur.com/4A2TF4P.png)

```bash
import { redirect } from "next/navigation";
import { NextRequest, NextResponse } from "next/server";


export async function GET(request:NextRequest) {

    
    return NextResponse.json(
        redirect("/")
    )
}
```
---
