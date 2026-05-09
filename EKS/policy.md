AWSLoadBalancerControllerIAMPolicy  
{
    "Effect": "Allow",
    "Action": [
        "elasticloadbalancing:DescribeListenerAttributes",
        "elasticloadbalancing:DescribeListeners",
        "elasticloadbalancing:DescribeLoadBalancers",
        "elasticloadbalancing:DescribeRules",
        "elasticloadbalancing:DescribeTags",
        "elasticloadbalancing:DescribeTargetGroups",
        "elasticloadbalancing:DescribeTargetHealth",
        "elasticloadbalancing:ModifyListener",
        "elasticloadbalancing:ModifyRule",
        "elasticloadbalancing:ModifyTargetGroupAttributes",
        "elasticloadbalancing:ModifyLoadBalancerAttributes"
    ],
    "Resource": "*"
}
and re-attach the policy 
aws iam attach-role-policy \
    --policy-arn arn:aws:iam::aws:policy/AmazonEKSALBIngressControllerPolicy \
    --role-name AmazonEKSLoadBalancerControllerRole
