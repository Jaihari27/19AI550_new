# Ex.No: 10  Implementation of 2D Coin Collector Game 
### DATE:08/09/2026                                                                           
### REGISTER NUMBER : 212225230109
### AIM: 
To develop a Coin Collector 2D game in Unity 
### Algorithm:

1. **Start**
2. Open **Unity Hub**.
3. Create a new **2D project**.
4. Create the game scene.
5. Add the **player**.
6. Add **ground, platforms, and obstacles**.
7. Add **coins or collectibles**.
8. Add player movement and jumping.
9. Add collision detection.
10. Add score and lives.
11. Add **Win** and **Game Over** conditions.
12. Test the game.
13. Fix errors if any.
14. Build and run the game.
15. **Stop**.

### Program:
```
```csharp
using UnityEngine;

public class PlayerMovement : MonoBehaviour
{
    public float speed = 5f;
    public float jumpForce = 7f;

    private Rigidbody2D rb;
    private bool isGrounded;

    void Start()
    {
        rb = GetComponent<Rigidbody2D>();
    }

    void Update()
    {
        float move = Input.GetAxis("Horizontal");

        rb.linearVelocity = new Vector2(move * speed, rb.linearVelocity.y);

        if (Input.GetKeyDown(KeyCode.Space) && isGrounded)
        {
            rb.linearVelocity = new Vector2(rb.linearVelocity.x, jumpForce);
        }
    }

    void OnCollisionEnter2D(Collision2D collision)
    {
        if (collision.gameObject.CompareTag("Ground"))
        {
            isGrounded = true;
        }
    }

    void OnCollisionExit2D(Collision2D collision)
    {
        if (collision.gameObject.CompareTag("Ground"))
        {
            isGrounded = false;
        }
    }
}
```

```
### Output:


### Result:
Thus the game was developed using Unity and adopted _-----------AI technology.
