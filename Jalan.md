using UnityEngine;

public class jalan : MonoBehaviour
{
    public float playerMoveSpeed = 10f;

    void Start()
    {
        transform.position = Vector3.zero;
        Debug.Log("This is called at first frame");
    }

    void Update()
    {
        if (Input.GetKey(KeyCode.A))
        {
            transform.position += Vector3.left * playerMoveSpeed * Time.deltaTime;
        }
        if (Input.GetKey(KeyCode.D))
        {
            transform.position += Vector3.right * playerMoveSpeed * Time.deltaTime;
        }
    }
}
