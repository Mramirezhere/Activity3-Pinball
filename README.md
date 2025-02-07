This is the destroy script I
                           V
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class DestroyScript : MonoBehaviour
{
    public GameObject GameManager;
    
    // Start is called before the first frame update
   

     private void OnCollisionEnter2D(Collision2D collision)
    {
                  
        if(collision.gameObject.tag == "Ball")
       {
            Destroy(collision.gameObject);
       }
    }  
      
}
This is Score Script I
                     V
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class ScoreScript : MonoBehaviour
{
          public int Score;
    public void OnCollisionEnter2D(Collision2D collision)
    {
  


        if(collision.gameObject.tag == "Bumper")
        {
            Score += 100;
        }
    }
}

This is Paddle Script I
                      V
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class PaddleScript : MonoBehaviour
{
    
        public Vector3 runleft;
     public Vector3 runright;

    // Update is called once per frame
    void Update()
    {
              if (Input.GetKey(KeyCode.A))
      {
        GetComponent<Transform>() .position += runleft;
      }
      if (Input.GetKey(KeyCode.D))
      {
        GetComponent<Transform>() .position += runright;
      }
    }
}
